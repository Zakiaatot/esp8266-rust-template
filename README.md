# esp8266-rust-template

**A very simple project template for esp8266 in `rust`.**

## Usage

### Clone template

`git clone https://github.com/Zakiaatot/esp8266-rust-template`

### Prepare toolchains

- [espup](https://github.com/esp-rs/espup) + [cargo-espflash](https://github.com/esp-rs/espflash):

```bash
cargo install espup
cargo install cargo-espflash
espup install 
. $HOME/export-esp.sh
```

### Compile

`cargo build --release`

### Flash

`cargo espflash --release --monitor /dev/ttyUSB*`

## Related links

- <https://github.com/esp-rs/esp8266-hal>
- <https://github.com/esp-rs/espup>
- <https://github.com/esp-rs/espflash>
