# Watermark Plugin for DITA Bootstrap


[![license](https://img.shields.io/github/license/jason-fox/fox.jason.watermark.svg)](http://www.apache.org/licenses/LICENSE-2.0)
[![DITA-OT 4.1](https://img.shields.io/badge/DITA--OT-4.1-blue.svg)](http://www.dita-ot.org/4.1)

This is a [DITA-OT Plug-in](https://www.dita-ot.org/plugins) to add a watermark to generated HTML. The plugin
extends the DITA Bootstrap HTML.

<details>
<summary><strong>Table of Contents</strong></summary>

-   [Install](#install)
    -   [Installing DITA-OT](#installing-dita-ot)
    -   [Installing the Plug-in](#installing-the-plug-in)
-   [Usage](#usage)
    -   [Parameter Reference](#parameter-reference)
-   [License](#license)

</details>

## Install

The DITA Bootstrap Watermark plug-in has been tested against [DITA-OT 3.x](http://www.dita-ot.org/download). It is recommended that
you upgrade to the latest version.

### Installing DITA-OT

<a href="https://www.dita-ot.org"><img src="https://www.dita-ot.org/images/dita-ot-logo.svg" align="right" height="55"></a>

The DITA Bootstrap Watermark plug-in is a plug-in for the DITA Open Toolkit.

-   Full installation instructions for downloading DITA-OT can be found
    [here](https://www.dita-ot.org/4.1/topics/installing-client.html).

    1.  Download the `dita-ot-4.1.zip` package from the project website at
        [dita-ot.org/download](https://www.dita-ot.org/download)
    2.  Extract the contents of the package to the directory where you want to install DITA-OT.
    3.  **Optional**: Add the absolute path for the `bin` directory to the _PATH_ system variable.

    This defines the necessary environment variable to run the `dita` command from the command line.

```console
curl -LO https://github.com/dita-ot/dita-ot/releases/download/4.1/dita-ot-4.1.zip
unzip -q dita-ot-4.1.zip
rm dita-ot-4.1.zip
```

### Installing the Plug-in

-   Run the plug-in installation commands:

```console
dita install fox.jason.extend.css
dita install net.infotexture.dita-bootstrap
dita install https://github.com/jason-fox/dita-bootstrap.watermark/archive/master.zip
```

The `dita` command line tool requires no additional configuration.

---

## Usage

The plugin extends Bootstrap HTML processing:

```console
PATH_TO_DITA_OT/bin/dita -f html5-bootstrap \
  -i document.ditamap \
  --bootstrap.watermark=draft|review|final|none
```

By default the output HTML will be watermarked as a **DRAFT**

### Parameter Reference

-   `bootstrap.watermark` - Decides which watermark to use:
    -   `draft` - Adds a watermark stating **DRAFT DOCUMENT**
    -   `review` - Adds a watermark stating _Copy for review only_
    -   `final` - Adds a sidebar footer only
    -   `none` - Does not add any watermarks


## License

[Apache 2.0](LICENSE) © 2023 Jason Fox
