# Configuration

- [Settings](#settings)
- [Documentation Directory](#documentation-directory)
- [Directory Structure](#directory-structure)
- [Meta file](#meta-file)

<a name="settings"></a>
## Settings

Set the desired environment variables so the package knows your image model, controller(s), etc. 

Example environment config:
```bash
DOC_WEAVER_ROUTE_PREFIX=docs
DOC_WEAVER_DIR=resources/docs
```

These variables, and more are explained within the [config](https://github.com/ReliQArts/laravel-doc-weaver/blob/master/src/config/config.php) file.

<a name="documentation-directory"></a>
### Documentation Directory

The documentation directory is the place where you put your project documentation directories. It may be changed with the config key `doc-weaver.storage.dir` or the environment variable `DOC_WEAVER_DIR`. The default documentation directory is `resources/docs`.

<a name="directory-structure"></a>
### Directory Structure

Each project directory should contain seperate folders for each documented version. Each version must have at least two (2) markdown files, namely `documentation.md` and `installation.md`, which serve as the sidebar and initial documentation pages respectively.

```bash
[doc dir]
    │
    └─── Project One
    │       └── 1.0 
    │       └── 2.1
    │            └── .docweaver.yml       # meta file (optional)
    │            └── documentation.md     # sidebar nav
    │            └── installation.md      # initial page
    │
    └─── Project Two
```

<a name="meta-file"></a>
### Meta File

Configurations for each doc version may be placed in `.docweaver.yml`. The supported settings are:
- #### name
    Product name.
- #### description
    Product description.

- #### image_url
    Product image url. This may be an absolute url (e.g. `http://mywebsite.com/myimage.jpg`) or an image found in the `images` resource directory.

    To use the `foo.jpg` in the images directory you would set `image_url` to `{{docs}}/images/foo.jpg`.

    For more info. see: [Assets](/docs/{{version}}/assets)