
# EntrarSemConta – Crie Conta Local no Windows Sem Microsoft

**Crie uma conta local durante a instalação do Windows 11 ou 10, sem precisar de internet e sem vincular à Microsoft.**

---

## ⚠️ Aviso de Responsabilidade

Este conteúdo é fornecido com fins técnicos e educacionais.  
Use apenas em sistemas sob sua responsabilidade.  
A Microsoft pode alterar ou bloquear esse comportamento em atualizações futuras.

---

## 🎯 Objetivo

Permitir que você ignore a exigência de conta Microsoft durante a instalação (OOBE) e crie uma **conta local offline**.

Ideal para:
- Ambientes corporativos
- Laboratórios
- Instalações técnicas
- Usuários que não querem depender de nuvem

---

## 💡 Como usar

Durante a instalação do Windows, na tela que exige conexão com a internet:

### 🔸 Método com script automático

1. Pressione `Shift + F10` para abrir o Prompt de Comando.
2. Digite:
   ```cmd
   oobe\bypassnro.cmd
   ```
3. O sistema será reiniciado.
4. Após o reboot, será possível criar uma **conta local** sem conexão.

> Este script está incluso no repositório.

---

### 🔸 Método manual (sem script)

1. Desconecte da internet (remova cabo/desligue Wi-Fi).
2. Na tela “Vamos conectar você a uma rede”, pressione `Shift + F10`.
3. Execute:
   ```cmd
   taskkill /f /im oobenetworkconnectionflow.exe
   ```
4. A tela será fechada e a criação de conta local será habilitada.

---

## 📁 Arquivos incluídos

- `bypassnro.cmd` – Script de bypass automático
- `README.md` – Este manual

---

## 🧠 Observações

- Funciona em Windows 10 e 11 (versões até o momento).
- A conta criada não será vinculada a serviços online.
- A Microsoft pode alterar esse processo em builds futuros.

---

## 📄 Licença

Distribuído sob a licença [MIT](LICENSE).  
Você pode usar, adaptar e redistribuir com os devidos créditos.

---

**Criado por [rivaed](https://github.com/rivaed) – controle local desde o primeiro boot.**
