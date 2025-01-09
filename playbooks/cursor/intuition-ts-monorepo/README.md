# Intuition TS Monorepo AI Helpers

This repository contains temporary AI helper configurations and documentation for the intuition-ts-monorepo. These files will eventually be integrated directly into the main monorepo, but for now, they serve as a stopgap workflow to improve AI assistance when working with the codebase.

## Contents

- `.cursorrules`: Configuration file for AI assistants to better understand our monorepo's conventions and requirements
- `ai-helpers/`: Directory containing specific guidance for common development patterns
  - `querying-data.md`: Guidelines for implementing data querying patterns in the monorepo

## Diagnostic Prompts and Syntax Keywords

The configuration includes special diagnostic and directive features:

### Diagnostic Prompts

- Files contain specific greeting prompts (e.g., "Hi friend! Let's collaborate!" in `.cursorrules`)
- These prompts serve as diagnostic tools to verify that the AI has properly loaded and is using the correct context
- When you see these greetings in AI responses, it confirms the configuration is active

### Syntax Keywords

- Files use directive keywords like "when user asks" to guide AI attention to specific documentation
- For example, the `querying-data.md` file is triggered when discussing data querying patterns
- These keywords help ensure consistent and contextually appropriate responses

## Setup Instructions

1. Clone the intuition-ts-monorepo:

   ```bash
   git clone [intuition-ts-monorepo-url]
   cd intuition-ts-monorepo
   ```

2. Copy the `.cursorrules` file to the root of the monorepo:

   ```bash
   cp path/to/this/repo/.cursorrules ./
   ```

3. Create an ai-helpers directory in the docs folder and copy the contents:
   ```bash
   mkdir -p docs/ai-helpers
   cp -r path/to/this/repo/ai-helpers/* docs/ai-helpers/
   ```

## Usage

Once set up, the AI assistants will:

- Follow the conventions and patterns specified in `.cursorrules`
- Reference the documentation in `docs/ai-helpers` when providing guidance
- Suggest solutions that align with our established patterns, particularly for data querying and frontend implementations

## Cursor Notepad Beta Integration

We're currently experimenting with Cursor's Notepad beta feature as an alternative way to integrate these AI helpers. The markdown documentation can be added directly to your Notepad for easier access and reference. More details about this integration will be shared soon.

https://docs.cursor.com/features/beta/notepads#overview

## Note

This is a temporary solution until these files are properly integrated into the intuition-ts-monorepo. The patterns and guidelines provided here should be treated as the source of truth for AI-assisted development in the meantime.
