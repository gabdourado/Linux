# Criando Ambiente Virtual Python no Linux 

Um **ambiente virtual em Python** é um recurso que permite criar um espaço isolado para seus projetos com a linguagem. Nesse ambiente, você pode **instalar dependências específicas** sem afetar as bibliotecas instaladas globalmente no seu sistema. Isso é útil para **evitar conflitos entre versões de pacotes** e para garantir que cada projeto tenha exatamente as dependências necessárias para funcionar.

Para Criar e Configurar um ambiente Virtual Python, basta seguir os seguintes passos:

### 0. Acesse o terminal 
```scss
Ctrl + Alt + T
```
 
### 1. Atualize os pacotes
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Verificando versão do Python 3.

O  módulo `venv` vem embutido no Python 3.3 ou superior. Para verificar se o Python 3.3 está instalado execute no terminal:
```bash
python3 --version
```

Caso o Python 3.3 não esteja instalado, execute:
```bash
sudo apt install python3
```

### 3. Instalar o venv (se necessário)

Caso a execução do **passo 5** falhar, instale `venv` na sua máquina:
```bash
sudo apt install python3-venv
```

### 4. Navegar até o diretório em que deseja criar o ambiente virtual
```bash
cd /caminho/para/seu/projeto
```

### 5. Criar o ambiente virtual venv

Substitua `nome_do_ambiente` pelo nome que quiser, como `env` ou `venv`:
```bash
python3 -m venv nome_do_ambiente # python3 -m venv env
```

### 6. Ativar o ambiente virtua
```bash
source nome_do_ambiente/bin/activate
```

### 7. Instale o pip (opcional, mas recomendado)

O `pip` é o gerenciador de pacotes do Python, usado para instalar bibliotecas.
```bash
sudo apt install python3-pip
```

### 8. Instalar pacotes dentro do ambiente

No ambiente virtual, você pode instalar pacotes específicos usando `pip`:
```bash
pip install nome_do_pacote # pip install pandas plotly numpy
```

### 9. Desativar o ambiente virtual

Quando terminar de usar o ambiente, desative-o com:
```bash
deactivate
```
