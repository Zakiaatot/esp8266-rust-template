# esp8266-rust-template

**A very simple project template for esp8266 in `rust`.**

## Usage

### Clone template

```shell
git clone https://github.com/Zakiaatot/esp8266-rust-template
```

### Prepare toolchains

- [espup](https://github.com/esp-rs/espup) + [cargo-espflash](https://github.com/esp-rs/espflash):

```shell
cargo install espup
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
