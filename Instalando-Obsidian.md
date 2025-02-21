# Instalando Obsidian no Linux (Ubuntu)

Vamos instalar o Obsidian usando o **Flatpak**. Flatpak é um sistema de distribuição de software para Linux que simplifica a instalação e execução de aplicativos, garantindo compatibilidade entre diferentes distribuições.

Para instalar o Flatpak basta seguir os seguintes passos:

### 0. Acesse o terminal
```scss
Ctrl + Alt + T
```

### 1. Atualize os pacotes
```bash
sudo apt update
```

### 2. Instale o Flatpak
```bash
sudo apt install flatpak
```

### 3. Adicione o repositório Flathub (se ainda não o fez)
```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

```

### 4. Verificando a versão do Flatpak
```bash
flatpak --version
```

Agora vamos instalar o **Obsidian**. Para isso, basta seguir os seguintes passos:

### 0. Instale o Obsidian
```bash
flatpak install flathub md.obsidian.Obsidian
```

### 1. Execute o Obsidian
```bash
flatpak run md.obsidian.Obsidian
```

Agora é só reiniciar a máquina e usar o Obsidian em seus projetos. 
