# Instalação do Chrome no Linux (Ubuntu)

Algumas distribuições Linux não incluem o Google Chrome como navegador padrão. Se você deseja instalá-lo no Ubuntu via terminal, siga os passos abaixo:
### 1. Baixar o pacote `.deb` do Google Chrome

Acesse o site oficial do Google Chrome para baixar a versão compatível com o Ubuntu  [Chrome - Download Oficial](https://www.google.pt/intl/pt-PT/chrome/?brand=FHFK&ds_kid=43700076570751463&gad_source=1&gclid=Cj0KCQiAwtu9BhC8ARIsAI9JHam_6aHJb48k90s5PmPwDgWNVLTnq3_ltpPw0muN609VQ3oVx-_ISygaAjUtEALw_wcB&gclsrc=aw.ds) ou utilize o comando `wget` no terminal para fazer o download diretamente:
```Shell
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```

### 2. Instalar o Google Chrome

Agora, instale o pacote `.deb` com o `dpkg`:
```Shell
sudo dpkg -i google-chrome-stable_current_amd64.deb # Dentro da pasta Downloads
```

Caso apareçam erros de dependências, corrija com:
```Shell
sudo apt-get install -f
```

### 3. Executar o Google Chrome

Após a instalação, você pode abrir o Chrome pelo terminal com:
```Shell
google-chrome
```

Ou acesse através do menu de aplicativos.
