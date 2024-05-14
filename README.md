# obsidian-md-html-export
Adapted from [the python script created by Klalle](https://github.com/klalle/ObsidianToHtmlConverter) for exporting [obsidian](https://obsidian.md/) Markdown files.
Can be exported to static (local) html (recursively adds all link/images), or to a folder of Markdown files that is ready to use as an Obsidian vault. This fork is more useful for the latter.
I (RyzenFromFire) added support for limiting the depth of the recursion, because the original script basically tried to pull my whole vault, which didn't go well.

The script has 3 optional parameters:
1. Export to HTML or not [**Y**/N]
    - **N**: Exports the chosen md-file to a new vault and bring all the images and linked md-files with it (recursively!)
        - Easily opened as a new vault in obsidian and everything just works!
    - **Y**: Exactly like above, but also create HTML files next to the MD files (with images and working links to other md.html files in vault)
        - The script puts an index.html-file in the root of the exported vault that is a direct link to your exported file.md.html for easy access
2. Download external images to local vault [**Y**/N] (if export to HTML is chosen)
    - **Y**: downloads all the images
    - **N**: normal link to external image that downloads when viewed
3. A maximum depth (default 5)

Run this script from the root of Obsidian vault.

usage: 
```python3 exportMdFileToHtml.py <filename.md> <[y/n] [y/n]>```
- "<filename.md>" **no filepath needed** unless you have several files with same name

Only tested on Linux and Windows!

