# Instalando o MySQL Workbench no Linux

Vamos instalar, no Linux - Ubuntu -, dois softwares para trabalharmos com banco de dados: o **MySQL** e o **MySQL Workbench**. O **MySQL** é um sistema de gerenciamento de banco de dados relacional que armazena e gerencia dados. O **MySQL Workbench** é uma ferramenta gráfica que facilita a administração e interação com o MySQL, permitindo criar bancos de dados, executar consultas e gerenciar dados de forma visual.

Para instalar o MySQL basta seguir os seguintes passos:

### 0. Acesse o terminal 

```scss
Ctrl + Alt + T
```

### 1. Atualize os pacotes

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Instale o MySQL
```bash
sudo apt install mysql-server -y
```

### 3. Verificando o Status do MySQL
```bash
sudo systemctl status mysql
```

O status deve mostrar `active (running)`. Para sair, pressione `q`.

### 4. Verificando a versão do MySQL
```bash
mysql --version
```


Agora vamos instalar o **MySQL Workbench**. Para isso, basta seguir os seguintes passos:

### 0. Baixar o MySQL Workbench

No site oficial do MySQL [https://dev.mysql.com/downloads/workbench/](https://dev.mysql.com/downloads/workbench/), baixe o arquivo `.deb` da versão compatível do MySQL Workbench compatível com a sua distribuição do Ubuntu.

### 1. Instale o MySQL Workbench
```bash
sudo dpkg -i mysql-workbench*.deb # Dentro da pasta Downloads 
```

### 2. Resolva as dependências (caso necessário)
```bash
sudo apt-get install -f
```

### 3. Verifique a instalação
```bash
mysql-workbench
```

Agora basta configurar e utilizar o **MySQL Workbench**.
