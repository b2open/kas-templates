# kas

Configuration files for playing demos and training environments with Toradex Colibri iMX8.


### Install kas

```
pipx install kas
```


## Download
```
git clone -b scarthgap https://github.com/b2open/kas-templates.git kas
```


## Build Toradex BSP 7.5.0 for Colibri iMX8

```
kas build kas/tb2-colibri-imx8x-bsp7-minimal.yml
```

With `--keep`:
```
kas build kas/tb2-colibri-imx8x-bsp7-minimal.yml -- -k
```

Open shell:
```
kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml.yml
```

Invoke bitbake manually:
```
kas shell kas/tb2-colibri-imx8x-bsp7-minimal.yml -c "bitbake minicom"
```



## Templates

| Files    | Description |
| -------- | ------- |
| tb2-colibri-imx8x-bsp7-debug.yml | Build using colibri-imx8x and tdx-reference-minimal-image for training |
| tb2-colibri-imx8x-bsp7-minimal.yml | Build using colibri-imx8x and tdx-reference-minimal-image supporting debugging tools for training |
| tb2-qemuarm-minimal.yml | Build using colibri-imx8x and core-image-minimal for training |


