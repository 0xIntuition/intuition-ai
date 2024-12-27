# Intuition GraphQL Query Assistant Rules

This repository contains a set of rules optimized for AI agents (particularly in Cursor's composer mode) to help query Intuition data effectively. The rules provide intelligent assistance for working with the `@0xintuition/graphql` package.

## Installation

1. If you already have a `.cursorrules` file:

   - Append the entire contents of `.cursorrules` from this repository to your existing file
   - Or copy specific rules you need into your existing `.cursorrules`

2. If you don't have a `.cursorrules` file:
   - Copy the `.cursorrules` file directly into your project root

## Features

- Framework-specific implementations (Next.js, Remix, Node.js)
- Intelligent query assistance for all Intuition data types
- Built-in error handling and optimization patterns
- Real-time update capabilities
- Type-safe query examples

## Sample Prompts

Here are some example prompts to help you get started:

### Basic Setup

```markdown
"I want to start querying Intuition data in my Next.js app. How do I set this up?"
```

```markdown
"How do I configure the GraphQL client for my Remix application?"
```

```markdown
"Show me how to set up the React Query provider for Intuition queries."
```

### Data Type Queries

```markdown
"How do I fetch positions for a specific account?"
```

```markdown
"Show me how to query atoms and their relationships."
```

```markdown
"I need to fetch triples that connect two specific atoms."
```

```markdown
"How can I get recent events for my application?"
```

```markdown
"Show me how to query the social graph and connections."
```

```markdown
"How do I fetch protocol-wide statistics?"
```

### Advanced Patterns

```markdown
"How can I combine multiple queries to build a profile page?"
```

```markdown
"Show me how to implement real-time updates for positions."
```

```markdown
"What's the best way to handle errors in Intuition queries?"
```

```markdown
"How do I optimize caching for frequently accessed data?"
```

### Framework-Specific Examples

#### Next.js

```markdown
"Show me how to implement SSR with Intuition queries in Next.js."
```

```markdown
"How do I handle loading states for Intuition data in my Next.js components?"
```

#### Remix

```markdown
"How do I use Intuition queries in my Remix loader functions?"
```

```markdown
"Show me how to handle errors with Intuition data in Remix."
```

#### Node.js/Express

```markdown
"How do I set up type-safe Intuition queries in my Express routes?"
```

```markdown
"Show me how to handle GraphQL errors in my Node.js application."
```

## Best Practices

1. **Framework Selection**

   - Always specify your framework when asking for help
   - Each framework has optimized patterns for data fetching

2. **Type Safety**

   - Use the provided TypeScript interfaces
   - Leverage the built-in type generation

3. **Error Handling**

   - Implement proper error boundaries
   - Use the provided error handling patterns

4. **Performance**

   - Utilize React Query's caching capabilities
   - Implement proper loading states
   - Use SSR when possible

5. **Real-time Updates**
   - Consider polling for frequently changing data
   - Use appropriate cache invalidation strategies

## Common Patterns

1. **Profile Pages**

   ```markdown
   "How do I build a profile page that shows:

   - User's atoms
   - Their connections
   - Recent activity
   - Position holdings"
   ```

2. **Social Feeds**

   ```markdown
   "How do I create a social feed that displays:

   - Connected users' activities
   - Recent events
   - Related positions"
   ```

3. **Analytics Dashboards**

   ```markdown
   "How do I build a dashboard showing:

   - Protocol-wide stats
   - User-specific metrics
   - Historical trends"
   ```

## Contributing

Feel free to suggest improvements or additional patterns by:

1. Opening an issue
2. Submitting a pull request
3. Suggesting new prompts or use cases

## Support

If you encounter any issues or need help:

1. Check the existing rules and examples
2. Try the sample prompts
3. Reach out to the Intuition team
