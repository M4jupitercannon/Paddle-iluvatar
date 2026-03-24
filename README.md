# PaddlePaddle for Iluvatar GPU

English | [简体中文](./README_cn.md)

Please refer to the following steps to compile, install and verify paddlepaddle_iluvatar.

## Compilation and Installation

```bash
# Please contact Iluvatar customer support (services@iluvatar.com) to obtain the SDK image

# Clone PaddleCustomDevice source code
git clone https://github.com/PaddlePaddle/Paddle-iluvatar.git

bash build_paddle.sh

# Install
bash install_paddle.sh
```

To enable CINN, set the CMake option **`WITH_CINN` to `ON`** (it is off by default), for example:

```bash
WITH_CINN=ON bash build_paddle.sh
```

## Incremental compilation (faster rebuilds after code changes)

```bash
# Incremental compilation (faster rebuilds after code changes, also installs whl)
bash build_inc.sh
```

For incremental builds with CINN enabled, pass the same variable:

```bash
WITH_CINN=ON bash build_inc.sh
```

## Verification

```bash
# Run tests
cd tests
bash run_test.sh
```
