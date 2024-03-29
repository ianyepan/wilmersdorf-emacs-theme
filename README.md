<h3 align="center">Wilmersdorf Emacs Theme</h3>
<hr/>


<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/EmacsIcon.svg/120px-EmacsIcon.svg.png" />
</p>

<p align="center">
<a href="https://github.com/ianpan870102/wilmersdorf-emacs-theme"><img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" alt="Maintenance"></a>
<a href="https://www.gnu.org/licenses/gpl-3.0"><img src="https://img.shields.io/badge/License-GPL%20v3-blue.svg" alt="GPL License"></a>
<a href="https://github.com/ianpan870102/.emacs.d"><img src="https://img.shields.io/github/release/ianpan870102/wilmersdorf-emacs-theme" alt="Version"></a>
<a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" alt="Awesome"></a>
</p>

<p align="center">An original Emacs theme with dark subtle syntax highlighting</p>

<p align="center">Inspired by Monochrome, Spacemacs Dark, Ariake Dark, and Raiju</p>

<br/>
<br/>

#### Note: This theme is now featured in the [doom-themes](https://github.com/hlissner/emacs-doom-themes) package as doom-wilmersdorf

#### Installation

##### Option 1. Manual install

Download `wilmersdorf-theme.el` and put it under `~/.emacs.d/themes/` (or `~/.config/emacs/themes/`), then add these lines to your `init.el`:

```
(add-to-list 'custom-theme-load-path "~/.emacs.d/themes/")
# or
(add-to-list 'custom-theme-load-path "~/.config/emacs/themes/")

(load-theme `wilmersdorf t)
```
##### Option 2. MELPA

Install the `doom-themes` package from MELPA, and load the `doom-wilmersdorf` theme.

#### Screenshots

<br/>
On macOS:
<br/>
<br/>

![alt text](./screenshots/posframe.png)

![alt text](./screenshots/solaire.png)

<br/>
On Arch Linux (WSL2):
<br/>

![alt text](./screenshots/elisp.png)

![alt text](./screenshots/neofetch.png)


#### Solaire-mode support

This theme supports solaire-mode. A sample configuration is as
follows:

```emacs-lisp
(use-package solaire-mode
  :hook ((change-major-mode . turn-on-solaire-mode)
         (after-revert . turn-on-solaire-mode)
         (ediff-prepare-buffer . solaire-mode)
         (minibuffer-setup . solaire-mode-in-minibuffer))
  :config
  (add-to-list 'solaire-mode-themes-to-face-swap '"wilmersdorf")
  (setq solaire-mode-auto-swap-bg t)
  (solaire-global-mode +1))

(with-eval-after-load 'solaire-mode
  (add-to-list 'custom-theme-load-path (concat user-emacs-directory "themes/"))
  (load-theme 'wilmersdorf t))
```

<br/>
<br/>

Copyright© 2018-2023 Ian Y.E. Pan

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see https://www.gnu.org/licenses/.
