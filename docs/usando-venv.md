
## 📌 O que é venv?  
O **venv** é uma ferramenta nativa do Python que cria um ambiente isolado para instalar pacotes sem interferir no sistema global. Isso ajuda a manter versões específicas de bibliotecas para cada projeto.  

---

## 🎯 1. Criando um Ambiente Virtual  

### 🔹 Verifique se você tem o Python instalado  
Abra o terminal e execute:  
```bash
python --version
```
ou  
```bash
python3 --version
```
Se retornar algo como `Python 3.x.x`, você está pronto para continuar.  

---

### 🔹 Criando o ambiente virtual  
No diretório do seu projeto (ex: `samu`), execute:  
```bash
python -m venv venv
```
Ou
```bash
python3 -m venv venv
```
Isso criará uma pasta chamada **venv/** contendo o ambiente virtual.  



---

## 🎯 2. Ativando o Ambiente Virtual  

### 🔹 No **Linux/macOS**  
No terminal, rode:  
```bash
source venv/bin/activate
```

### 🔹 No **Windows (cmd ou PowerShell)**  
No **CMD** (Prompt de Comando):  
```cmd
venv\Scripts\activate
```
No **PowerShell**:  
```powershell
venv\Scripts\Activate.ps1
```
Após ativação, você verá algo assim no terminal:  
```bash
(venv) user@pc:~/samu$
```
Isso indica que o ambiente virtual está ativo. ✅  

---

## 🎯 3. Instalando Dependências  

Agora que o ambiente virtual está ativo, instale o Django e outras dependências do projeto:  
```bash
pip install django
```
Para salvar as dependências instaladas em um arquivo:  
```bash
pip freeze > requirements.txt
```
Isso gera um arquivo `requirements.txt` com algo assim:  
```
Django==4.2
```
Agora, qualquer pessoa pode recriar o mesmo ambiente rodando:  
```bash
pip install -r requirements.txt
```

---

## 🎯 4. Desativando o Ambiente Virtual  
Para sair do ambiente virtual, rode:  
```bash
deactivate
```

---

## 🎯 5. Ativando Automaticamente no Terminal (Opcional)  
Se quiser ativar o **venv** automaticamente ao entrar no diretório do projeto, edite o `.bashrc` ou `.zshrc` e adicione:  
```bash
cd ~/samu && source venv/bin/activate
```
Agora, toda vez que abrir o terminal no projeto, o ambiente virtual será ativado. 🚀  

---

## 🎯 Recapitulando os Comandos  
```bash
# Criar um ambiente virtual
python -m venv venv

# Ativar no Linux/macOS
source venv/bin/activate

# Ativar no Windows (CMD)
venv\Scripts\activate

# Instalar pacotes
pip install xxx

# Salvar dependências
pip freeze > requirements.txt

# Instalar dependências de um projeto existente
pip install -r requirements.txt

# Desativar o ambiente virtual
deactivate
```

