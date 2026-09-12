# Corne Keymap

## Layer 0 — Default

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ TAB │  Q  │  W  │  E  │  R  │  T  │   │  Y  │  U  │  I  │  O  │  P  │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│CTRL │  A  │  S  │  D  │  F  │  G  │   │  H  │  J  │  K  │  L  │  ;  │  '  │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│SHFT │  Z  │  X  │  C  │  V  │  B  │   │  N  │  M  │  ,  │  .  │  /  │ ESC │
└─────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │ GUI │ LWR │ SPC │   │ ENT │ RSE │ ALT │
                  └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

## Layer 1 — Lower (`LWR`, held)

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ TAB │  1  │  2  │  3  │  4  │  5  │   │  6  │  7  │  8  │  9  │  0  │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│CAPS │ BT1 │ BT2 │ BT3 │ BT4 │ BT5 │   │LEFT │DOWN │ UP  │RIGHT│  ·  │  ·  │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│SHFT │ F1  │ F2  │ F3  │ F4  │ F5  │   │ F6  │ F7  │ F8  │ F9  │ F10 │ F11 │
└─────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │ GUI │  ·  │ SPC │   │ ENT │  ·  │ ALT │
                  └─────┴─────┴─────┘   └─────┴─────┴─────┘
```
`CAPS` = `&kp CAPS` (new — was `&trans`, sits between the Tab row and the Shift row)
`BT1`–`BT5` = `&bt BT_SEL 0..4` (switch Bluetooth profile, non-destructive)
`·` = `&trans` (falls through to the layer below)

## Layer 2 — Raise (`RSE`, held)

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ TAB │  !  │  @  │  #  │  $  │  %  │   │  ^  │  &  │  *  │  (  │  )  │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│CTRL │EMOJI│PREV │ PP  │NEXT │  ·  │   │  -  │  =  │  [  │  ]  │  \  │  `  │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│SHFT │MUTE │VOL- │VOL+ │BRI- │BRI+ │   │  _  │  +  │  {  │  }  │  |  │  ~  │
└─────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │ GUI │  ·  │ SPC │   │ ENT │  ·  │ ALT │
                  └─────┴─────┴─────┘   └─────┴─────┴─────┘
```
Media row moved down from `CTRL` row to `SHFT` row.
`PREV`/`PP`/`NEXT` = `&kp C_PREV` / `&kp C_PP` / `&kp C_NEXT` (new)
`EMOJI` = `&kp LC(LG(SPACE))` (Ctrl+Cmd+Space, macOS's real emoji-picker shortcut). Replaces an earlier attempt at `&kp GLOBE` (ZMK's emulated Apple Fn key, [zmk#1938](https://github.com/zmkfirmware/zmk/pull/1938)) — that keycode gets silently dropped unless `CONFIG_ZMK_HID_CONSUMER_REPORT_USAGES_FULL=y` is set, and is still flaky on macOS even then, so a plain modifier combo is the reliable choice.

## Layer 3 — Adjust (`LWR` + `RSE` held together, tri-layer)

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│  ·  │  ·  │  ·  │  ·  │  ·  │  ·  │   │  ·  │  ·  │  ·  │  ·  │  ·  │  ·  │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│BTCLR│  ·  │  ·  │  ·  │  ·  │  ·  │   │  ·  │  ·  │  ·  │  ·  │  ·  │BOOT │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│  ·  │  ·  │  ·  │  ·  │  ·  │  ·  │   │  ·  │  ·  │  ·  │  ·  │  ·  │  ·  │
└─────┴─────┴─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │  ·  │  ·  │  ·  │   │  ·  │  ·  │  ·  │
                  └─────┴─────┴─────┘   └─────┴─────┴─────┘
```
`BTCLR` = `&bt BT_CLR` (forgets current Bluetooth bond — now needs both thumb layers + one finger, not just one thumb)
`BOOT` = `&bootloader` (reboot into UF2 flashing mode)
