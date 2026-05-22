# kas

Configuration files for playing demos and training environments with Toradex Colibri iMX8.


### Install kas

```
pipx install kas==5.2.0
```


## Download
```
git clone -b scarthgap https://github.com/b2open/kas-templates.git kas
```


## Build Toradex BSP 7.5.0 for Colibri iMX8

```
kas build kas/tb2-colibri-imx8x-bsp7-minimal.yml
```

Build another image recipe, example: `tdx-reference-multimedia-image`:
```
kas build kas/tb2-colibri-imx8x-bsp7-minimal.yml --target tdx-reference-multimedia-image
```

With `--keep`:
```
kas build kas/tb2-colibri-imx8x-bsp7-minimal.yml -- -k
```

Open shell:
```
kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml
```

Invoke bitbake manually:
```
kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml -c "bitbake minicom"
```

Generate SDK:
```
kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml -c populate_sdk
```

Get environment (alternatives):
```
kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml -c "bitbake -e tdx-reference-minimal-image"

kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml -- --environment
```


## Templates

| Files    | Description |
| -------- | ------- |
| tb2-colibri-imx8x-bsp7-debug.yml | Build using colibri-imx8x and tdx-reference-minimal-image for training |
| tb2-colibri-imx8x-bsp7-minimal.yml | Build using colibri-imx8x and tdx-reference-minimal-image supporting debugging tools for training |
| tb2-qemuarm-minimal.yml | Build using colibri-imx8x and core-image-minimal for training |


