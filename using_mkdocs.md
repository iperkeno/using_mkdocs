# Using mkdocs v.20200301

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

	open browser at: `http://127.0.0.1:8000`
	
    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Special Markdown features

!!! warning 
	this is a *warning*

!!!	notes 
	this is a *note*
	

[wxWidget Manual]( /xwWidgets.pdf )

[web]( https://fontawesome.com/icons/link?style=solid )

## **_mkdocs** directory
In order to have all makdocs files in the same directory,
we create this structure:
```
└─┬

/docs-root-dir
	│
	├── file-1
	├── ..
	├── ..
	├── file-n
	│
	└──/_mkdocs
		│
		├─ mkdocs.yaml
		├─ extra.css
		├─ markdown_style.css
		├─ .. other stylesheets
		└─ using_mkdocs.md

```


inside mkdocs.yaml define docs directory as the parent of yaml file,
define the extra css directory as the _mkdocs directory itself:

```yaml
	docs_dir: ".."

	extra_css:
		- "/_mkdocs/extra.css"
```
## Serve multiple mkdocs
Using command `make serve` the docs on the default port **8000**


In order to serve multiple mkdocs repositories is necessary to specify for each one
a different address:port couple:
```	
	mkdocs serve --dev-addr localhost:9000
```

## mkdocs PDF

[mkdocs-with-pdf](https://pypi.org/project/mkdocs-with-pdf/)


