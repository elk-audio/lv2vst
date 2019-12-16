# lv2vst

Modified for headless plugin build for [Elk Audio OS](https://elk.audio)

## Building Instructions

1. Set up the cross-compilation toolchain:  

   ```bash
   $ unset LD_LIBRARY_PATH
   $ source /opt/elk-sika64-sdk/environment-setup-aarch64-elk-linux
   ```

2. Use `make` to build the plugin.

## Using

For every lv2 plugin a dedicated folder needs to be created. In the folder put the `lv2vst.so` and create a `.whitelist` file with the plugin you wish to load. In sushi set the path to point to the `lv2vst.so` file and put the type as `vst2x`.

## Additional notes

* If the plugin is able to load make sure the folder where your `.lv2` folder is stored is part of the `LV2_PATH` variable.
* For further compilation help. Look at our [documentation](https://github.com/elk-audio/elk-docs/blob/master/documents/building_plugins_for_elk.md).