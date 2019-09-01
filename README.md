# DIY Bitcoin Hardware

On this website you can find links to interesting DIY bitcoin and lightning-related projects. This includes hardware wallets, verification tools, POS terminals, full nodes and other stuff.

If you want your project to be inluded on the website please open a pull request [on github](https://github.com/diybitcoinhardware/diybitcoinhardware.github.io)

# Hardware wallets

## Real hardware wallets

If you are not scared of soldering you can build any of existing open-source hardware wallets like Trezor or Coldcard. Building your own wallet reduces risks of supply chain attack and gives you all the benefits of a normal hardware wallet.

### Trezor

- [Making your own Trezor](https://www.instructables.com/id/Making-My-Own-Trezor-Crypto-Hardware-Wallet/)
- [Trezor firmware repo](https://github.com/trezor/trezor-firmware)
- [Trezor hardware repo](https://github.com/trezor/trezor-hw) - PCB designs & case

### ColdCard

- [Firmware](https://github.com/Coldcard/firmware)
- Hardware design is not available (?)

## DIY hardware wallets

DIY hardware wallets are not as secure as real ones, but they can be easily tuned for your needs and sometimes have very unique ux and security features.

### Work In Progress

These wallets are still in development, so they may not have all the functionality planned by the authors yet, but it's worth to keep an eye on their progress.

- [Specter](https://github.com/cryptoadvance/specter-diy) (Mbed framework) - DIY airgapped hardware wallet that uses QR codes for communication with the host. Based on STM32F469I-DISCO developer board.
- [BitBoy](https://github.com/justinmoon/bitboy) (Micropython) - a hardware wallet based on M5Stack dev board.
- [Koopa](https://github.com/arcbtc/koopa) (Arduino) - 15$ watch-only hardware wallet that uses E-Ink display to show your next receiving address. Makes sense to take with you if you plan to receive money to your cold storage while keeping your real hardware wallet safe.

### Archive

Here we put links to interesting projects that look abandoned / discontinued, mostly for educational and curiosity reasons.

- [Hardware Bitcoin Wallet](https://github.com/someone42/hardware-bitcoin-wallet) by someone42 - a 7 (!!!) years old repo, probably the very first hardware wallet ever
- [8bkc-wally](https://github.com/greenaddress/8bkc-wally/) - a hardware wallet for PocketSprite using libwally library (by GreenAddress)
- [Simple hardware wallet](https://github.com/arduino-bitcoin/simple_hardware_wallet) (Arduino) - a hardware wallet based on Adafruit M0 board, includes web UI that talks to the wallet over WebUSB
- [M5stack hardware wallet](https://github.com/stepansnigirev/m5stack_hardware_wallet) (Arduino) - a minimal hardware wallet based on M5Stack that talks to your computer over Bluetooth Serial

# Point of sale terminals

TBD

# Full nodes

TBD

- Raspiblitz etc

# Libraries

- [trezor-crypto](https://github.com/trezor/trezor-firmware/tree/master/crypto) - Trezor crypto library
- [mbed-tls](https://github.com/ARMmbed/mbedtls) - general purpose crypto library that includes elliptic curve crypto, hash functions and other stuff necessary for Bitcoin wallet, but doesn't have any bitcoin-specific things (like base58 encoding etc)
- [micro-bitcoin](https://github.com/micro-bitcoin/uBitcoin) - C++ bitcoin library compatible with Arduino, Mbed and bare metal
- [modcryptocurrency](https://github.com/Coldcard/modcryptocurrency) - ColdCard micropython bindings of Trezor crypto library
- [libwally](https://github.com/ElementsProject/libwally-core/) - C library with wallet primitives by Blockstream (not so easy to run on embedded system)