# edu-powermenu

A graphical rofi-based power menu (logout / shutdown / restart / lock / suspend) for window-manager setups that don't ship a built-in one. Rebrand of the original ArcoLinux powermenu, part of the `~/EDU/` learning series.

## What's in this repo

- `usr/bin/` or `usr/local/bin/` — the `edu-powermenu` launcher script.
- `etc/skel/` — keybinding hints / desktop integration assets.
- `setup.sh`, `up.sh` — standard EDU bash scaffold.

## Installation

### From `nemesis_repo` (recommended)

```ini
[nemesis_repo]
SigLevel = Never
Server = https://erikdubois.github.io/$repo/$arch
```

```bash
sudo pacman -Syu
sudo pacman -S edu-powermenu
```

You'll also need rofi (the menu front-end):

```bash
sudo pacman -S rofi
```

### Manual

```bash
git clone https://github.com/erikdubois/edu-powermenu.git
cd edu-powermenu
sudo cp -r usr/. /usr/
sudo cp -r etc/skel/. /etc/skel/
```

## Usage

Bind `edu-powermenu` to a key in your WM config (Super+X is a common choice):

```
super + x
    edu-powermenu
```

Or run it from a terminal:

```bash
edu-powermenu
```

## Websites

Information : https://erikdubois.be

## Social Media

Youtube : https://www.youtube.com/erikdubois

## License

See [LICENSE](./LICENSE).
