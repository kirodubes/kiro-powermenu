<p align="center">
  <img src="kiro.jpg" alt="Kiro" width="220" />
</p>

# kiro-powermenu

A graphical rofi-based power menu (logout / shutdown / restart / lock / suspend) for window-manager setups that don't ship a built-in one. Rebrand of the original ArcoLinux powermenu, part of the `~/EDU/` learning series.

## What's in this repo

- `usr/bin/` or `usr/local/bin/` — the `kiro-powermenu` launcher script.
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
sudo pacman -S kiro-powermenu
```

You'll also need rofi (the menu front-end):

```bash
sudo pacman -S rofi
```

### Manual

```bash
git clone https://github.com/kirodubes/kiro-powermenu.git
cd kiro-powermenu
sudo cp -r usr/. /usr/
sudo cp -r etc/skel/. /etc/skel/
```

## Usage

Bind `kiro-powermenu` to a key in your WM config (Super+X is a common choice):

```
super + x
    kiro-powermenu
```

Or run it from a terminal:

```bash
kiro-powermenu
```

## Websites

Information : https://erikdubois.be

## Social Media

Youtube : https://www.youtube.com/erikdubois

<!-- KIRO-FUNDING-FOOTER:START — managed by Kiro-HQ/cascade-readme-footer.sh -->
## Help fund Kiro

Everything I build here stays free and open — always. If Kiro or any of these
tools have ever saved you time or taught you something, a small monthly
contribution helps keep the work going. Donations target break-even, nothing
more — the core always stays free for everyone.

- GitHub Sponsors: https://github.com/sponsors/erikdubois
- Patreon: https://www.patreon.com/c/kiroproject
- YouTube memberships: https://www.youtube.com/@ErikDubois/join
- Ko-fi: https://ko-fi.com/erikdubois
- PayPal: https://www.paypal.me/erikdubois
<!-- KIRO-FUNDING-FOOTER:END -->

## License

See [LICENSE](./LICENSE).
