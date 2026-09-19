# KATSEYE - Kawaii Glyph Rain

A VGA demo for [Tiny Tapeout](https://tinytapeout.com) built with the IHP shuttle template. Columns of kawaii symbols rain down the screen, and the message **"KATSEYE RULES"** is revealed in the center, one letter at a time.

Built in [VGA Playground](https://vga-playground.com) and hardened into an ASIC with Tiny Tapeout.

## What it does

- Falling 8x8 pixel glyphs: hearts, stars, sparkles, flowers, cats, music notes, smileys and moons
- Columns fall at two different speeds, with a bright white head and a fading trail
- After a short delay, "KATSEYE RULES" appears in the center of the screen
- Each letter flashes white, then settles into a shimmering pastel color
- A framed plate with a color-cycling border sits behind the text
- Four pastel palettes: sakura pink, mint soda, lavender dream and peach cream
- 640x480 VGA output at 25.175 MHz with 6-bit color (2 bits per channel)

## Pinout

| Pin | Function |
|-----|----------|
| `ui[1:0]` | Palette select (00 sakura pink, 01 mint soda, 10 lavender dream, 11 peach cream) |
| `ui[7:6]` | VGA mode |
| `uo[0]` | R1 |
| `uo[1]` | G1 |
| `uo[2]` | B1 |
| `uo[3]` | VSYNC |
| `uo[4]` | R0 |
| `uo[5]` | G0 |
| `uo[6]` | B0 |
| `uo[7]` | HSYNC |

This is the standard TinyVGA PMOD layout.

## Hardware needed

- Tiny Tapeout demo board
- TinyVGA PMOD
- VGA monitor

## Source code

- [tt_um_vga_glyph_mode.v](src/tt_um_vga_glyph_mode.v) (top module `tt_um_vga_glyph_mode`)
- [hvsync_generator.v](src/hvsync_generator.v) (VGA timing generator)

Direct link: https://github.com/cleajane/katseye-bootcamp/blob/main/src/tt_um_vga_glyph_mode.v

More detail on how the design works is in [docs/info.md](docs/info.md).

## Author

CLEA

## License

Apache-2.0 (see the `LICENSE` file).

## About Tiny Tapeout

Tiny Tapeout is an educational project that makes it easier and cheaper than ever to get your digital and analog designs manufactured on a real chip. Learn more at https://tinytapeout.com.
