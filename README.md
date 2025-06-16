# @ohos-rs/abort-controller

AbortController for OpenHarmony based on `emitter`.

> The bulk of the code in this project is derived from [node-abort-controller](https://github.com/southpolesteve/node-abort-controller), with certain alterations made to suit the features of HarmonyOS.

![Platform](https://img.shields.io/badge/platform-arm64/arm/x86__64-blue) ![API Version](https://img.shields.io/badge/MIN--OpenHarmony--API-12-green)

## Install

```shell
ohpm install @ohos-rs/abort-controller
```

## Usage

```ts
const controller = new AbortController();

asyncFib(20, controller.signal).catch((e: ESObject) => {
    console.error(e) // Error: AbortError
})

controller.abort()
```