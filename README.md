# dircolors Themes

Reusable `dircolors` profiles and palette helpers for ANSI-slot-based terminals.

This repository currently includes:

- [`pastel.dircolors`](./pastel.dircolors): custom Pastel `dircolors` profile
- [`pastel_palette.sh`](./pastel_palette.sh): shell exports for the Pastel palette and default profile colors
- [`pastel_ls_colors_preview.sh`](./pastel_ls_colors_preview.sh): static `LS_COLORS` preview for the Pastel profile
- [`nord.dircolors`](./nord.dircolors): Nord-based `dircolors` profile

## Usage

Apply a profile directly with `dircolors`:

```bash
eval "$(dircolors -b ./pastel.dircolors)"
eval "$(dircolors -b ./nord.dircolors)"
```

Load the Pastel palette metadata into your current shell:

```bash
source ./pastel_palette.sh
echo "$PASTEL_PROFILE_FOREGROUND_HEX"
echo "$PASTEL_ANSI_12_HEX"
```

## ANSI Palette Note

`dircolors` only emits ANSI SGR codes such as `34`, `95`, or `44`. The final appearance therefore depends on how your terminal maps ANSI color slots `0` through `15`.

- The Pastel profile ships its intended slot values in [`pastel_palette.sh`](./pastel_palette.sh).
- The Nord profile assumes the standard `nord0` through `nord15` mapping used by the upstream [Nord project](https://www.nordtheme.com/) and its [color palette documentation](https://www.nordtheme.com/docs/colors-and-palettes/).

## Pastel

Pastel is a soft custom palette with a very dark background, a bright off-white foreground, and low-harshness accent colors for the 16 ANSI terminal slots.

### Profile Colors

| Sample                                          | Role       | #    | ANSI               | Hex       | RGB           |
|-------------------------------------------------|------------|------|--------------------|-----------|---------------|
| ![Pastel foreground](img/pastel-foreground.svg) | Foreground | `fg` | default foreground | `#eff0f3` | `239 240 243` |
| ![Pastel background](img/pastel-background.svg) | Background | `bg` | default background | `#191a1c` | `25 26 28`    |

### ANSI Palette

| Sample                                    | Role           | #    | ANSI       | Hex       | RGB           |
|-------------------------------------------|----------------|------|------------|-----------|---------------|
| ![Pastel ANSI 0](img/pastel-ansi-0.svg)   | Black          | `0`  | `30 / 40`  | `#1e1f22` | `30 31 34`    |
| ![Pastel ANSI 1](img/pastel-ansi-1.svg)   | Red            | `1`  | `31 / 41`  | `#f89494` | `248 148 148` |
| ![Pastel ANSI 2](img/pastel-ansi-2.svg)   | Green          | `2`  | `32 / 42`  | `#b2e4a7` | `178 228 167` |
| ![Pastel ANSI 3](img/pastel-ansi-3.svg)   | Yellow         | `3`  | `33 / 43`  | `#ffef9f` | `255 239 159` |
| ![Pastel ANSI 4](img/pastel-ansi-4.svg)   | Blue           | `4`  | `34 / 44`  | `#a9c7f1` | `169 199 241` |
| ![Pastel ANSI 5](img/pastel-ansi-5.svg)   | Magenta        | `5`  | `35 / 45`  | `#cfbaf0` | `207 186 240` |
| ![Pastel ANSI 6](img/pastel-ansi-6.svg)   | Cyan           | `6`  | `36 / 46`  | `#96c2c6` | `150 194 198` |
| ![Pastel ANSI 7](img/pastel-ansi-7.svg)   | White          | `7`  | `37 / 47`  | `#f1edfb` | `241 237 251` |
| ![Pastel ANSI 8](img/pastel-ansi-8.svg)   | Bright black   | `8`  | `90 / 100` | `#393b40` | `57 59 64`    |
| ![Pastel ANSI 9](img/pastel-ansi-9.svg)   | Bright red     | `9`  | `91 / 101` | `#fda5ac` | `253 165 172` |
| ![Pastel ANSI 10](img/pastel-ansi-10.svg) | Bright green   | `10` | `92 / 102` | `#b9fbc0` | `185 251 192` |
| ![Pastel ANSI 11](img/pastel-ansi-11.svg) | Bright yellow  | `11` | `93 / 103` | `#fdffb6` | `253 255 182` |
| ![Pastel ANSI 12](img/pastel-ansi-12.svg) | Bright blue    | `12` | `94 / 104` | `#b1e5f7` | `177 229 247` |
| ![Pastel ANSI 13](img/pastel-ansi-13.svg) | Bright magenta | `13` | `95 / 105` | `#f1c7e9` | `241 199 233` |
| ![Pastel ANSI 14](img/pastel-ansi-14.svg) | Bright cyan    | `14` | `96 / 106` | `#c0fdff` | `192 253 255` |
| ![Pastel ANSI 15](img/pastel-ansi-15.svg) | Bright white   | `15` | `97 / 107` | `#fcfcfc` | `252 252 252` |

## Nord

Nord is an arctic, north-bluish palette created by the [Nord project](https://www.nordtheme.com/) and documented in the official [colors and palettes reference](https://www.nordtheme.com/docs/colors-and-palettes/). The `nord.dircolors` file in this repository follows the canonical `nord0` through `nord15` slot numbering used for terminal color compatibility.

| Sample                      | Token    | #    | ANSI       | Hex       | Palette     |
|-----------------------------|----------|------|------------|-----------|-------------|
| ![Nord 0](img/nord-0.svg)   | `nord0`  | `0`  | `30 / 40`  | `#2e3440` | Polar Night |
| ![Nord 1](img/nord-1.svg)   | `nord1`  | `1`  | `31 / 41`  | `#3b4252` | Polar Night |
| ![Nord 2](img/nord-2.svg)   | `nord2`  | `2`  | `32 / 42`  | `#434c5e` | Polar Night |
| ![Nord 3](img/nord-3.svg)   | `nord3`  | `3`  | `33 / 43`  | `#4c566a` | Polar Night |
| ![Nord 4](img/nord-4.svg)   | `nord4`  | `4`  | `34 / 44`  | `#d8dee9` | Snow Storm  |
| ![Nord 5](img/nord-5.svg)   | `nord5`  | `5`  | `35 / 45`  | `#e5e9f0` | Snow Storm  |
| ![Nord 6](img/nord-6.svg)   | `nord6`  | `6`  | `36 / 46`  | `#eceff4` | Snow Storm  |
| ![Nord 7](img/nord-7.svg)   | `nord7`  | `7`  | `37 / 47`  | `#8fbcbb` | Frost       |
| ![Nord 8](img/nord-8.svg)   | `nord8`  | `8`  | `90 / 100` | `#88c0d0` | Frost       |
| ![Nord 9](img/nord-9.svg)   | `nord9`  | `9`  | `91 / 101` | `#81a1c1` | Frost       |
| ![Nord 10](img/nord-10.svg) | `nord10` | `10` | `92 / 102` | `#5e81ac` | Frost       |
| ![Nord 11](img/nord-11.svg) | `nord11` | `11` | `93 / 103` | `#bf616a` | Aurora      |
| ![Nord 12](img/nord-12.svg) | `nord12` | `12` | `94 / 104` | `#d08770` | Aurora      |
| ![Nord 13](img/nord-13.svg) | `nord13` | `13` | `95 / 105` | `#ebcb8b` | Aurora      |
| ![Nord 14](img/nord-14.svg) | `nord14` | `14` | `96 / 106` | `#a3be8c` | Aurora      |
| ![Nord 15](img/nord-15.svg) | `nord15` | `15` | `97 / 107` | `#b48ead` | Aurora      |

## Sources

- Pastel values are defined locally in [`pastel_palette.sh`](./pastel_palette.sh).
- Nord palette values come from the official [Nord project](https://www.nordtheme.com/) and its [Colors and Palettes documentation](https://www.nordtheme.com/docs/colors-and-palettes/).
