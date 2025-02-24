# Instalação do Vim no Linux (Ubuntu)
O **Vim** (_Vi IMproved_) é um editor de texto altamente configurável e poderoso, criado para sistemas Unix. Ele é amplamente utilizado por programadores e administradores de sistemas devido à sua eficiência e versatilidade.


Para instalação do Vim, basta seguir os seguintes passos
### 0. Acesse o terminal 
```scss
Ctrl + Alt + T
```
 
### 1. Atualize os pacotes
```bash
sudo apt update && sudo apt upgrade
```

### 2. Instale o Vim
```shell
sudo apt install vim
```

### 3. Verificando a versão do Vim
```shell
vim --version
```


Para configurar inicialmente o Vim, você pode usar as seguintes diretivas: 
### 0. Crie o arquivo `~/.vimrc` (caso não criado)
```shell
touch ~/.vimrc
```

### 1. Abra o arquivo no Vim
```shell
vim ~/.vimrc
```

### 2. Adicione as seguintes configurações básicas

```vim
" ativar sintaxe colorida
syntax on

" ativar indentação automática
set autoindent

" ativa indentação inteligente
set smartindent

" ativar numeração de linha
set number

" destaca a linha em que o cursor está posicionado
set cursorline

" ativa o clique do mouse para navegação pelos documentos
set mouse=a

" ativa o compartilhamento de área de transferência entre o Vim
" e a interface gráfica
set clipboard=unnamedplus

" converte o tab em espaços em branco
" ao teclar tab o Vim irá substutuir por 2 espaços
set tabstop=2 softtabstop=2 expandtab shiftwidth=2

" Tema escuro para melhor visibilidade
set background=dark
```

Para adicionar Plugins, siga os seguintes passos:
### 0. Crie o diretório para adicionar os Plugins
```shell
mkdir -p .vim/pack/git-plugins/start # No seu diretório Home
```

### 1. Entrar no diretório criado
```shell
cd .vim/pack/git-plugins/start
```
### 2. Clonar os Plugins do `GitHub`
* Personalização da tela inicial do Vim

```shell
git clone https://github.com/mhinz/vim-startify
```

*  Personalização das Cores/Temas do Vim
```shell
git clone https://github.com/rafi/awesome-vim-colorschemes
```
Alterando o arquivo  `~/.vimrc`
```vim
color materialbox " Ou outro tema que você prefira
```

* Melhorando a indentação no código com 'barrinhas'
```shell
git clone https://github.com/Yggdroot/indentLine
```
Alterando o arquivo  `~/.vimrc`
```vim
let g:indentLine_enabled = 1
```

* Visualizando Diretórios em formato de Árvore
```shell
git clone https://github.com/preservim/nerdtree
```
Alterando o arquivo  `~/.vimrc`
```vim
map <C-n> :NERDTreeToggle<cr> " Ctrk + n
set encoding=utf8
```

* Modificando os ícones dos diretórios e arquivos
```shell
git clone https://github.com/ryanoasis/vim-devicons
```
Instale uma fonte de sua preferência em [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) seguindo os passos a seguir:
```sheel
/tmp/FiraCodeNerdFont-Regular.ttf # Salve na pasta tmp durante do Download
```
Acessando pasta de fonts:
```shell
mkdir ~/.fonts/ # Verificando se o diretório já não existe
cd ~/.fonts/ #  Acessando o diretório de fonts
```
Copiando fonte baixada para o diretório de fonts:
```shell
cp /tmp/FiraCodeNerdFont-Regular.ttf .
```
Atualizando as fonts existentes:
```sheel
fc-cache
```

Obtendo o nome da fonte escolhida:
```shell
fc-list | grep Fira 
```

Alterando o arquivo  `~/.vimrc`
```vim
set guifont=FiraCode\ Nerd\ Font:h12
```

* Mostrando o arquivo que está aberto
```shell
git clone https://github.com/vim-airline/vim-airline
git clone https://github.com/vim-airline/vim-airline-themes
```

Alterando o arquivo  `~/.vimrc`
```vim
set laststatus=2
let g:airline#extensions#tabline#enabled = 1
let g:airline_powerline_fonts = 1
let g:airline_statusline_ontop=0
let g:airline_theme='base16_twilight'
let g:airline#extensions#tabline#formatter = 'default'

" navegação entre os buffers
nnoremap <M-Right> :bn<cr>
nnoremap <M-Left> :bp<cr>
nnoremap <c-x> :bp\|bd #<cr>
```

Após todas as alterações, recarregue sua máquina com o comando `reboot`:
```shell
reboot
```

### 7. Atalhos Essenciais no Vim

#### Modo de inserção

Pressione `i` para inserir texto.
#### Modo normal

Pressione `ESC` para sair do modo de inserção.
#### Salvar arquivo

Execute `:w nome-do-arquivo` no modo de comando.
```vim
:w nome-do-arquivo
```
#### Sair do Vim

Execute `:q` no modo de comando.
```vim
:q
```
#### Salvar e sair

Execute `:wq` ou `ZZ` no modo de comando.
```vim
:wq
```
#### Sair sem salvar

Execute `:q!` no modo de comando.
```vim
:q!
```
#### Copiar linha

Pressione `yy` no modo de comando
#### Colar

Pressione `p` no modo de comando.
#### Desfazer 

Pressione `u` no modo de comando.
#### Refazer

Pressione `Ctrl + r` no modo de comando.
#### Pesquisar

Execute `:/palavra` e pressione `n` para próxima ocorrência no modo de comando.
```vim
:/palavra
```
