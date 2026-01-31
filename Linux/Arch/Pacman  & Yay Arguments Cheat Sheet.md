

| Flag          | Meaning / Usage                                       | Example                                       |
| ------------- | ----------------------------------------------------- | --------------------------------------------- |
| `-R`          | Remove package                                        | `sudo pacman -R package`                      |
| `-Rs`         | Remove package + unneeded dependencies                | `sudo pacman -Rs package`                     |
| `-Rns`        | Remove package + unneeded dependencies + config files | `sudo pacman -Rns package`                    |
| `-S`          | Sync / install package                                | `sudo pacman -S package`                      |
| `-Sy`         | Refresh package database only                         | `sudo pacman -Sy`                             |
| `-Syu`        | Refresh database + upgrade all packages               | `sudo pacman -Syu`                            |
| `-U`          | Install package from a local file                     | `sudo pacman -U /path/to/package.pkg.tar.zst` |
| `-Ss`         | Search for a package in the repositories              | `pacman -Ss package`                          |
| `-Qs`         | Search for installed package                          | `pacman -Qs package`                          |
| `-Qi`         | Show info about an installed package                  | `pacman -Qi package`                          |
| `-Si`         | Show info about a repo package                        | `pacman -Si package`                          |
| `-Sw`         | Download a package without installing                 | `pacman -Sw package`                          |
| `-Su`         | Upgrade all packages                                  | `pacman -Su`                                  |
| `-Sc`         | Clean cached packages not installed                   | `pacman -Sc`                                  |
| `-Scc`        | Clean **all** cached packages                         | `pacman -Scc`                                 |
| `-Q`          | List installed packages                               | `pacman -Q`                                   |
| `-Qe`         | List explicitly installed packages                    | `pacman -Qe`                                  |
| `-Qd`         | List dependencies                                     | `pacman -Qd`                                  |
| `-Qdt`        | List orphaned packages                                | `pacman -Qdt`                                 |
| `-Qm`         | List foreign / AUR packages                           | `pacman -Qm`                                  |
| `-Qn`         | List packages from repos                              | `pacman -Qn`                                  |
| `-Qo`         | Find which package owns a file                        | `pacman -Qo /usr/bin/bash`                    |
| `--needed`    | Skip reinstalling up-to-date packages                 | `pacman -S --needed package`                  |
| `--noconfirm` | Auto-confirm prompts                                  | `pacman -Syu --noconfirm`                     |
