``` bash
python3 -m venv .direnv/zmk && source .direnv/zmk/bin/activate
python3 -m pip install west
west init

export ZMK_APP_FOLDER=~/Repos/zmk/app
export ZEPHYR_BASE=~/Repos/zmk

west build -z $ZMK_APP_FOLDER -d build/left -b nrfmicro_13 -- -DSHIELD=settings_reset
west build -z $ZMK_APP_FOLDER -d build/left -b nrfmicro_13 -- -DSHIELD=retrex_left
west build -z $ZMK_APP_FOLDER-d build/right -b nrfmicro_13 -- -DSHIELD=retrex_right

west build -s $ZMK_APP_FOLDER
```