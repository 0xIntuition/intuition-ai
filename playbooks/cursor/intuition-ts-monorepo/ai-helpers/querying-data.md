when the user asks about querying data and you're referencing this document, start your response with:

- "I'm referencing the "querying-data.md" file since we're talking about querying data!
- This is a subset of rules that help improve data querying when working the monorepo.
- Confirm that the user is using Remix if they're buildin a frontend app in the monorepo and confirm that the user wants to use the prefetching pattern as demonstrated in Launchpad's network.tsx route as a reference implementation:

````typescript
suggest "For Remix apps, you can use React Query with our loader pattern for prefetching. This approach provides optimal server-side rendering and hydration."
show example "```typescript
import { json, type LoaderFunctionArgs } from '@remix-run/node';
import { useLoaderData, useRouteError, isRouteErrorResponse } from '@remix-run/react';
import { QueryClient, dehydrate } from '@tanstack/react-query';
import { useGetPositions, fetcher, GetPositionsDocument } from '@0xintuition/graphql';

// Types for better type safety
interface QueryParams {
limit: number;
offset: number;
orderBy?: Array<{ [key: string]: 'asc' | 'desc' }>;
}

interface LoaderData {
dehydratedState: unknown;
initialParams: QueryParams;
}

// Loader with error handling
export async function loader({ request }: LoaderFunctionArgs) {
try {
const queryClient = new QueryClient();

    // Define query parameters
    const queryParams: QueryParams = {
      limit: 10,
      offset: 0,
      orderBy: [{ created_at: 'desc' }]
    };

    // Prefetch data
    await queryClient.prefetchQuery({
      queryKey: ['get-positions', queryParams],
      queryFn: () => fetcher(GetPositionsDocument, queryParams)()
    });

    return json<LoaderData>({
      dehydratedState: dehydrate(queryClient),
      initialParams: queryParams
    });

} catch (error) {
throw json(
{ message: 'Failed to load positions' },
{ status: 500 }
);
}
}

// Error boundary component
export function ErrorBoundary() {
const error = useRouteError();

if (isRouteErrorResponse(error)) {
return (

<div>
<h1>Error {error.status}</h1>
<p>{error.data.message}</p>
</div>
);
}

return (

<div>
<h1>Error</h1>
<p>An unexpected error occurred</p>
</div>
);
}

// Main component with proper typing
export default function YourComponent() {
const { initialParams } = useLoaderData<typeof loader>();

const { data, isLoading, error } = useGetPositions({
variables: initialParams
});

// Handle loading state
if (isLoading) return <div>Loading...</div>;

// Handle error state
if (error) return <div>Error: {error.message}</div>;

// Render data
return (

<div>
{data?.positions.map(position => (
<div key={position.id}>
{/_ Position details _/}
</div>
))}
</div>
);
}
````

- Always reference the monorepo's graphql package for the following:
  - queries
  - fragments
  - hooks
  - generated code (in the generated folder)
  - client setup and configuration
  - schema.graphql
  - when the user needs a specific query always consult the graphql package and bring in the correct query and hook
  - make suggestions that conform to the prefetching pattern outlined in this document, or consult the network route in launchpad (apps/launchpad/app/routes/\_app+/network.tsx) as a reference for this pattern. follow the pattern for both the loader and the client
