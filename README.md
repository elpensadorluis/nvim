# SENTU Neovim con vitaminas para Flutter dev


## Instalar con un solo comando

El siguiente comando instalará la configuración de Nvim y si tienes un existente configuración se creará un backup en `~/.config/nvim.old`

"Este scrpit solo soporta: Arch Linux, Ubuntu y Mac"

```
bash <(curl -s https://raw.githubusercontent.com/elpensadorluis/nvim/master/utils/install.sh)
```

## Instalar Neovim
- Arch

  ```
  sudo pacman -S neovim

  yay -S neovim-git # Latest
  ```

- Ubuntu

  ```
  sudo apt install neovim
  ```

- Mac

  ```
  brew install neovim

  brew install --HEAD neovim # Latest
  ```


## Clone esta configuración en tu sistema operativo

```
git clone https://github.com/elpensadorluis/nvim.git ~/.config/nvim
```

## Instalar soporte para python y node

```
pip install pynvim
```

```
npm i -g neovim
```

## Instalar Neovim remote

```
pip install neovim-remote
```

Esto instalará `nvr` en `~/.local/bin` entonces necesitaras agregar lo siguiente en `bashrc` o `zshrc`

```
export PATH=$HOME/.local/bin:$PATH
```

## Instalar soporte a clipboard

- En MacOs ya viene soportado

- Ubuntu

  ```
  sudo apt install xsel
  ```

- Arch

  ```
  sudo pacman -S xsel
  ```

## (Optional) Instalar soporte para python y node usando entornos virtuales

"Asegurate de tener las direcciones correctas a tu entorno"

```
let g:python3_host_prog = expand("<path to python with pynvim installed>")
let g:python3_host_prog = expand("~/.miniconda/envs/neovim/bin/python3.8") " <- ejemplo

let g:node_host_prog = expand("<path to node with neovim installed>")
let g:node_host_prog = expand("~/.nvm/versions/node/v12.16.1/bin/neovim-node-host") " <- ejemplo
```

## Listas de programas que deberías instalar

- ranger
- ueberzug
- ripgrep
- silver_searcher
- fd
- universal-ctags
- lazy git
- lazy docker


## Language Servers

CoC no soporta todos los lenguajes en su extensión, por ello recomiendo instalar algunos lenguajes desde cero y añadirlo al archivo `coc-settings.json` 

Ejemplo:

- bash

  `npm i -g bash-language-server`

  ```
  "languageserver": {
  "bash": {
    "command": "bash-language-server",
    "args": ["start"],
    "filetypes": ["sh"],
    "ignoredRootPaths": ["~"]
    }
  }
  ```

## Para que FAR funcione

```
:UpdateRemotePlugins
```

## TabNine

Para usar TabNine, ingrese lo siguiente en un búfer:

```
TabNine::config
```

**IMPORTANTE:** Esta extensión va a deborar tu memoria...

## Vim Gists

Para usar **vim-gists** necesitarás configurar lo siguiente:

```
git config --global github.user <username>
```

## TODO

- Mejorar la Documentación

## CoC extensión a probar:

- coc-fzf
- coc-stylelintplus
- coc-floaterm
- coc-actions
- coc-bookmark

## 0.1

- native lsp
- treesitter