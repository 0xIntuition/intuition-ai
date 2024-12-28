# Optimized Prompt for PDF Splitting Task

## Task Description

I have a PDF document that I need split into smaller, manageable chunks for processing or integration with large language models (LLMs). Each chunk should meet the following criteria:

1. **File Size**: Must be less than 2 MB.
2. **Line Limit**: Content should not exceed 250 lines.
3. **Order Preservation**: Chunks should preserve the original document's order and integrity.

## Expected Output

- **Downloadable Links**: Provide downloadable links for each chunk or a ZIP file containing all chunks.
- **Content Verification**: Ensure that chunks begin and end logically (e.g., no empty or incomplete content).
- **Quality Assurance**: Review chunks to confirm accuracy before delivery.

## Additional Information

- **Use Cases**: This process is particularly useful for preparing documents for LLM compatibility or scenarios where file size and line limits are critical.
- **Customization**: Adjust file size or line limits based on the specific requirements of your project.
- **Common Issues to Address**:
  - Avoid creating empty or corrupt chunks.
  - Ensure content flows logically across chunks.
  - Provide clear and accessible download links.

## Example Tools and Steps

1. **Splitting Tool**: Use a PDF processing library (e.g., PyPDF2) or similar tools.
2. **Verification**: Extract and review text from the first few chunks to ensure correctness.
3. **Packaging**: Bundle the chunks into a ZIP file for easy distribution if the number of files is large.

## Metadata

- Original File: [filename]
- Total Chunks: [number]
- Chunk Sequence: [X of Y]
- Related Chunks: [previous/next references]
- Last Updated: [date]

## AI Processing Optimization

- Maintain semantic coherence within chunks
- Include sufficient context overlap between chunks (recommended 2-3 sentences)
- Preserve hierarchical structure markers (headers, sections, subsections)
- Add chunk relationship indicators
- Ensure each chunk maintains enough context to be independently processable

## Validation Checklist

- [ ] Chunks maintain semantic completeness
- [ ] Headers and section markers are preserved
- [ ] Cross-references are properly maintained
- [ ] Metadata is complete and accurate
- [ ] Chunks can be processed independently
- [ ] Context overlap is sufficient between chunks

## Integration Notes

### Document Hierarchy

- Maintain consistent header levels across chunks
- Preserve parent-child relationships between sections
- Include breadcrumb trails for deep hierarchies

### Cross-References

- Use relative references between chunks when possible
- Maintain a reference map for complex documents
- Include forward/backward chunk references

### Version Control

- Track chunk modifications separately
- Maintain chunk sequence integrity
- Document any reordering or merging of chunks

### Best Practices

- Split at natural section boundaries when possible
- Preserve table and figure references
- Include minimal but sufficient context in each chunk
- Consider LLM token limits when determining chunk sizes

---

This template can be reused or modified to fit other file-splitting and processing needs.
