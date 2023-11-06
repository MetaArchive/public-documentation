# public-documentation

This site uses GitHub Pages's native Jekyll engine to render Markdown.
You can view the live site [here](https://metaarchive.github.io/public-documentation/)

Refer to the [Jekyll docs](https://jekyllrb.com/docs/configuration/options/) for availabe site configuration options.
The chosen theme is a lightly edited version of the [Minimal theme](https://github.com/pages-themes/minimal).

Each page shows a Page Tree in the sidebar.
The sidebar groups pages, but only at the top-level. Nesting more than one level deep is not supported.

New pages may be added by creating new markdown files in the appropriate folder.
They must indicate a title in order to display correctly in the page tree.
This can be done by setting Jekyll-style front matter or by starting the file with the title, underlined with equal signs (`=`)

New folders may be added by creating a folder (e.g. `new_folder`) and an accompanying Markdown page suffixed with `-index` (e.g. `new_folder-index.md`)
Pages in subfolders will be grouped alongside the rest of the folder content.
See [Building a Plugin](https://github.com/MetaArchive/public-documentation/blob/main/MetaArchive%20Cooperative/Technical%20Workflows/Ingest%20Content/Building%20a%20Plugin.md) for an example of titling the page to clarify its subfolder status.
