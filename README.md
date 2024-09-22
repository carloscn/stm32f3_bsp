# Test STM32F3

https://www.st.com/en/evaluation-tools/stm32f3discovery.html#overview

## Toolchains:
* https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads
* Note1 : recommand the 13.3.Rel1
* Note2 : linux system, can use `curl -sk https://raw.githubusercontent.com/carloscn/script/master/down_tool_chains/down_toolchain_13.2-rel1.sh | bash`

## Compile code

1. Config your cross compile tool path in `prj.cfg`
2. `source prj.cfg`
3. `git submodule update --init --recursive`
4. `make -j8`

## Donwload code

There are `st_flash` and `stm32cube_programmer` for your selection:
1. Link your stm32 into the host's usb.
2. `bash install_st_flash.sh` or download https://www.st.com/en/development-tools/stm32cubeprog.html
3. `bash flash.sh` (by config `USE_ST_FLASH` in `flash.sh`)

Note,
* stm32cubeprog can be supported by MAC-OS/WIN/Linux
* st-flash can be supported by WIN and Linux.

The program auto runs.