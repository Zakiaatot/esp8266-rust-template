# esp8266-rust-template

**A very simple project template for esp8266 in `rust`.**

## Usage

`Attention!` Only pass the test in `Ubuntu 22.04`

### Clone template

```shell
git clone https://github.com/Zakiaatot/esp8266-rust-template
```

### Prepare toolchains

- rust (nightly is better):

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

- xtensa-lx106-elf-gcc (for esp8266 cpu):

[reference](https://docs.espressif.com/projects/esp8266-rtos-sdk/en/latest/get-started/linux-setup.html)

```shell
mkdir -p ~/esp
cd ~/esp
curl -O https://dl.espressif.com/dl/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-linux-amd64.tar.gz
tar -xzf ./xtensa-lx106-elf-*
export PATH="$PATH:$HOME/esp/xtensa-lx106-elf/bin"
```

- [espup](https://github.com/esp-rs/espup) + [cargo-espflash](https://github.com/esp-rs/espflash):

```shell
cargo install espup
cargo install cargo-espflash
espup install 
. $HOME/export-esp.sh
```

or

```shell
cargo install binstall
cargo binstall espup
cargo install cargo-espflash
espup install 
. $HOME/export-esp.sh
```

### Compile

```shell
cargo build --release
```

### Flash

```shell
cargo espflash --release --monitor /dev/ttyUSB*
```

## Related links

- <https://github.com/esp-rs/esp8266-hal>
- <https://github.com/esp-rs/espup>
- <https://github.com/esp-rs/espflash>
- <https://docs.espressif.com/projects/esp8266-rtos-sdk/en/latest/get-started/linux-setup.html>
