# SkyKings Documentation Source
Contains the source of https://docs.skykings.net.

For documentation errors, please open an issue.

For modifications to the documentation, feel free to open a pull request.

## Editing the Docs

Documentation is build using the [Sphinx](https://www.sphinx-doc.org/en/master/) documentation generator. 
he documentation is written in [Markdown](https://www.markdownguide.org/) and uses 
[MyST](https://myst-parser.readthedocs.io/en/latest/) for compatibility with Sphinx.

### Installation

**Python 3.10+ is required.**

To install dependencies, run the following command:
- On Windows: `py -m pip install -r requirements.txt`
- On Linux: `python3 -m pip install -r requirements.txt`

### Contributing (Locally)

The documentation is stored in the `[source](source)` directory. 
`index.md` is the main page of the documentation, and 
`conf.py` contains the configuration for the documentation.

Once you have made your changes, you should preview them. 
You can use the following command to build the documentation:

Windows:

```bash
py -m sphinx -b html source build
```

Linux:

```bash
python3 -m sphinx -b html source build
```

The documentation will be built in the `build` directory. 
You can open the `index.html` file in your browser to preview the documentation.

Once done, make a pull request with your changes.


### Contributing (GitHub Web Editor)

You can also edit the documentation directly on GitHub. To do so, click on the file you want to edit, 
and then click on the pencil icon in the top right corner. Once done, make a pull request with your changes.

Once your pull request is made, you can preview the changes on Cloudflare Pages, 
through the link posted in a comment on your pull request.