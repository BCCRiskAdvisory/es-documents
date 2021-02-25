# es-documents

Sample documentation for 2021 TCD SWENG Documentation System project (

This repo contains sample documents for the purposes of testing the documentation system on something similar to what will be used in production.

**NOTE** most of the details below are proposals only, and depending on the implementation of the project, it might make sense to do things differently. Feel free to propose changes if they'll make the implementation easier.

## Folder Structure

The proposed folder structure for documents is:

- docs/
  - document/
    - 1_section_name/
      - 1_chapter_name.md
      - 2_chapter_name.md
      - image1.png
    - 2_section_name/
      - 1_chapter_name.md
      - 2_chapter_name.md
      - 3_chapter_name.md
  - document/
    - 1_section_name/
    - etc....

Some points to note:

- Ordering will be enforced lexicographically (i.e with leading numbers for each section/chapter)
- Chapters will be markdown documents
- Each markdown document will contain its own titles, subsections etc, as well as images and tables
-
- In freshdesk mode each level of the folder structure will map as follows:
  - document -> knowledge base
  - section -> folder
  - chapter -> article/page
- In PDF mode each level of the folder structure will map as follows:
  - document -> individual pdf document
  - section -> section
  - chapter -> chapter

## Links

One of the main requirements of the project is that links between pages are preserved. The proposed link format is:

```html
<a data-reference="document:section:chapter"></a>
```

- It's not necessary to support linking to a subsection within a chapter, only the chapter itself.
- We're taking advantage of the markdown specification being very permissive with HTML, `<a>` tags should be easy to pick out and transform.
- Links between documents won't be possible in PDF mode, it's an open question what would work well here.
- The link text should be the title of the chapter we're referring to

Once again, this is a proposal, there is no existing body of documents to import so we can tailor them to whatever works well in the system you provide.
