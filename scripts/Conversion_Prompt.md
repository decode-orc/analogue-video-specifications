# Conversion Prompt

Combine all individual markdown files from the new documentation folder into a single markdown document at the top level.

Ensure the following steps are performed in sequence (as appropriate - skip any that do not apply):

1. **Combine Files**: Verify that all individual page files from `<path>/pages/` are included in the new single markdown document. Place all images referenced in the markdown files under a sub-folder named `assets/`.

2. **Clean Up**: Once the combined document is verified, remove the original `<path>/pages/` folder.

3. **Remove Page Numbering and Headers/Footers**: Strip all page numbering headers/footers and general page headers/footers from the combined markdown document, retaining only the section headers.

4. **Format Figure Labels**: Ensure that all figure labels (e.g., "FIGURE x" or "Fig. X") are placed directly under their respective images.
   - Each figure label must be on its own line, separated by a newline from the image reference if necessary.

5. **Standardize Markdown Headings**: Ensure that all markdown heading levels are consistent to allow mkdocs to correctly build the Table of Contents (ToC). Remove any existing ToC in the markdown, as it will be replaced by the mkdocs ToC.

6. **Update Navigation and Documentation**: 
   - Include the new combined document in the mkdocs navigation configuration (e.g., `mkdocs.yml`).
   - Update the top-level `index.md` to reference the new document.
   - Add a link to the new document in the `README.md` file.
