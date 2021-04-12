# Tuneando la Shell

__Instalar PowerLine-Shell__
[https://github.com/b-ryan/powerline-shel](https://github.com/b-ryan/powerline-shell "PowerLine Shell")

``` # pip install powerline-shell```


__Instalar NeoFectch| ScreeenFectch__

[https://github.com/dylanaraps/neofetch](https://github.com/dylanaraps/neofetch "NeoFetch")

``` # apt-get install neofetch``` 

__Instalar Fonts PowerLine__

[https://github.com/powerline/fonts](https://github.com/powerline/fonts "FontsPowerLine")

``` # apt-get install fonts-powerline```


__Crear la carpeta y configuracion basica__

mkdir -p ~/.config/powerline-shell && \
powerline-shell --generate-config > ~/.config/powerline-shell/config.json


__Configurar el .bashrc__

```$ vim .bashrc```

```bash
function _update_ps1() {
    PS1=$(powerline-shell $?)
}

if [[ $TERM != linux && ! $PROMPT_COMMAND =~ _update_ps1 ]]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```


__VIM__

```# vim /etc/vim/.vimrc ```

```bash
set  rtp+=/usr/local/lib/python2.7/dist-packages/powerline/bindings/vim/
set laststatus=2
set t_Co=256
```
