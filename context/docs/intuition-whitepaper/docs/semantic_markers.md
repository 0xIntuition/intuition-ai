# Semantic Markers Reference

This document defines the semantic markup system used in the Intuition Protocol documentation to enhance machine readability while maintaining human readability.

## Purpose

Semantic markers serve to:

- Enable precise parsing by AI agents
- Maintain document structure
- Define relationships between concepts
- Support automated reasoning
- Facilitate information retrieval

## Marker Types

### Document Metadata

```
@metadata {
  version: string,          // Document version
  type: string,            // Document type (e.g., "specification", "guide")
  scope: string,           // Content scope
  intended_readers: string[], // Target audience
  semantic_version: string  // Semantic versioning
}
```

### Section Summaries

```
@section_summary {
  purpose: string,         // Section's main purpose
  key_components: string[], // Core components covered
  relationships: string[]  // Related concepts
}
```

### Concept Definitions

```
@concept {
  name: string,           // Concept name
  type: string,           // Concept type
  description: string,    // Brief description
  related: string[]       // Related concepts
}
```

### Relationships

```
@relationship {
  type: string,           // Relationship type
  source: string,         // Source concept
  target: string,         // Target concept
  properties: object      // Additional properties
}
```

## Usage Guidelines

### 1. Document Level

- Place @metadata at the start
- Include @key_concepts list
- Define main @relationships
- Specify @dependencies

### 2. Section Level

- Start with @section_summary
- Define local @concepts
- Specify @relationships
- Include @examples

### 3. Content Level

- Mark @terms inline
- Use @reference for citations
- Include @note for clarifications
- Mark @code_example

## Examples

### Document Header

```
@metadata {
  version: "1.0",
  type: "protocol_specification",
  scope: "trust_computation",
  intended_readers: ["ai_agents", "humans"],
  semantic_version: "1.0.0"
}

@key_concepts: [
  "trust_computation",
  "semantic_data",
  "economic_incentives"
]
```

### Section Example

```
@section_summary {
  purpose: "Defines core protocol components",
  key_components: ["Atoms", "Triples"],
  relationships: ["composition", "inheritance"]
}

@concept {
  name: "Atom",
  type: "core_component",
  description: "Fundamental unit of data",
  related: ["Triple", "Vault"]
}
```

## Best Practices

### 1. Consistency

- Use standard marker formats
- Maintain hierarchical structure
- Follow naming conventions
- Keep relationships explicit

### 2. Clarity

- Use descriptive names
- Provide complete metadata
- Include clear descriptions
- Maintain context

### 3. Completeness

- Define all key concepts
- Specify all relationships
- Include necessary context
- Document assumptions

### 4. Maintainability

- Use consistent formatting
- Keep markers updated
- Document changes
- Version appropriately

## Processing Guidelines

### For AI Agents

1. Parse metadata first
2. Build concept graph
3. Follow relationships
4. Maintain context
5. Validate understanding

### For Human Editors

1. Follow marker syntax
2. Maintain consistency
3. Update relationships
4. Verify completeness
5. Document changes
