# libwally and secp256k1 on Arduino and Mbed

[secp256k1](https://github.com/bitcoin-core/secp256k1/) and [libwally](https://github.com/ElementsProject/libwally-core) are the two most popular C libraries for Bitcoin.

[secp256k1](https://github.com/bitcoin-core/secp256k1/) is a de-facto standard way to do elliptic curve arithmetics — it has bindings to most languages (python, rust, javascript) and used in many software wallets.

[libwally](https://github.com/ElementsProject/libwally-core) is a C library used in Blockstream's projects like c-lightning, green address and many others. It includes a bunch of useful primitives for wallets and pretty well documented.

I didn't see many projects using this libraries on embedded devices though (Trezor, ColdCard, Keepkey and many other vendors are using trezor-crypto library).

If you are an experienced embedded developer it's not that hard to make these libraries to work on your device. But if you are a tinkerer and you want to experiment, if you are mostly playing with Arduino, ESP32 or Mbed devboards, and you want to make some fun hardware project involving Bitcoin, you may have problems with these libraries.

Normally in Arduino or Mbed you just drag-and-drop the library to the libraries folder, load an example, press the compile button in the IDE and it just works. With these libs it's not quite the case. But it is possible.

To make it happen we cloned repos of these libraries and slightly tuned them such that Arduino and Mbed could understand the folder structure and compile everything automatically. We also wrote basic examples for these libs — now you can do exactly what you always did — just drag and drop, load an example and start tuning it for your project.

**Warning**: these libraries are still pretty memory and flash intensive, so not every microcontroller and devboard will work. We tested it on ESP32 (M5Stack) and stm32f469-dicsovery boards. You will need a 32-bit microcontroller with enough memory and flash. I guess you need at least 512 kB of flash and 64 kB of RAM, with 2 MB flash and 256 kB RAM you will feel pretty comfortable.

## Repositories for Arduino and Mbed

- [secp256k1](https://github.com/diybitcoinhardware/secp256k1-embedded)
	- [Arduino example](https://github.com/diybitcoinhardware/secp256k1-embedded/blob/master/examples/basic_example/basic_example.ino)
	- [Mbed project](https://os.mbed.com/users/diybitcoinhardware/code/secp256k1_example/)
- [libwally](https://github.com/diybitcoinhardware/libwally-embedded)
	- [Arduino example](https://github.com/diybitcoinhardware/libwally-embedded/blob/master/examples/wally_example/wally_example.ino)
	- [Mbed project](https://os.mbed.com/users/diybitcoinhardware/code/libwally_example/)

Have fun, and let us know if it does or doesn't work :)

**Everyone was able to write his own software wallet, now everyone should be able to make a hardware wallet!**

_by [@StepanSnigirev](https://twitter.com/StepanSnigirev) and [@CryptoAdvance](https://twitter.com/CryptoAdvance)_
