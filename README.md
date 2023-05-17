# This is the camp-vim

Clone this repository.

Easy nvchad config can be run with docker:

```
docker run -w /root -it --rm debian:latest sh -uelic '                                                                                                                                                                  ─
  apt-get update
  apt-get install -y wget git nodejs npm build-essential
  wget https://github.com/neovim/neovim/releases/download/v0.9.0/nvim-linux64.tar.gz
  tar xvf nvim-linux64.tar.gz
  git clone https://github.com/NvChad/NvChad ~/.config/nvim
  cd nvim-linux64/bin
  bash
  '
```
