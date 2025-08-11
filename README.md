# 📚 Guia Prático de Git

**Controle de versão de forma clara e descomplicada**

Este guia foi criado para servir como um **manual rápido** de Git, focado em quem quer aprender **fazendo**.
Ele traz explicações simples, exemplos comentados e um fluxo de trabalho que você pode aplicar hoje mesmo no seu projeto.

---

## 🚀 1. O que é o Git?

O Git é um **sistema de controle de versão distribuído**.
Ele registra **cada mudança** que você faz no seu projeto, permitindo voltar no tempo, comparar versões e colaborar com outras pessoas.

> 📌 Pense no Git como um "histórico completo" do seu código, mas muito mais poderoso que o Ctrl+Z.

---

## 🧠 2. Conceitos Fundamentais

| Conceito               | O que é                                              | Analogia                                           |
| ---------------------- | ---------------------------------------------------- | -------------------------------------------------- |
| **Repositório (repo)** | O local onde seu código e histórico ficam guardados. | Um “armário” com todas as versões do seu projeto.  |
| **Commit**             | Registro de uma mudança no projeto.                  | Uma foto que você tira do projeto naquele momento. |
| **Branch**             | Linha independente de desenvolvimento.               | Um “universo paralelo” para testar ideias.         |
| **Merge**              | Combinar mudanças de uma branch em outra.            | Misturar dois textos mantendo o sentido.           |
| **Clone**              | Copiar um repositório existente para sua máquina.    | Baixar uma pasta inteira com histórico.            |
| **Push**               | Enviar suas mudanças para o repositório remoto.      | Publicar seu trabalho online.                      |
| **Pull**               | Baixar as mudanças que estão no repositório remoto.  | Atualizar seu projeto com novidades.               |

---

## 🔄 3. Fluxo de Trabalho no Git

1. **Criar ou clonar um repositório**
2. **Fazer mudanças no código**
3. **Adicionar arquivos para “área de preparação” (stage)**
4. **Fazer um commit (registrar a mudança)**
5. **Enviar para o repositório remoto (push)**
6. **Receber mudanças de outros (pull ou fetch)**

---

## 🛠 4. Comandos Básicos

### 4.1 Criar um novo repositório

```bash
git init
```

📌 Cria um repositório Git na pasta atual.
Após isso, o Git começa a rastrear mudanças na pasta.

---

### 4.2 Clonar um repositório existente

```bash
git clone https://github.com/usuario/repositorio.git
```

📌 Baixa o projeto **completo** (código + histórico) para sua máquina.
Após o clone, você terá uma pasta igual ao projeto original, pronta para modificar.

---

### 4.3 Verificar status do repositório

```bash
git status
```

📌 Mostra quais arquivos foram modificados e quais ainda não estão preparados para commit.
Exemplo de saída:

```
modified: index.html
untracked: style.css
```

> Untracked significa que o Git ainda não está rastreando o arquivo.

---

### 4.4 Adicionar arquivos para commit

```bash
git add arquivo.txt      # Adiciona apenas um arquivo
git add .                # Adiciona todos os arquivos modificados
```

📌 A partir daqui, o arquivo está **no stage**, pronto para ser “fotografado” no commit.

---

### 4.5 Criar um commit

```bash
git commit -m "Mensagem descritiva"
```

📌 Registra as mudanças no histórico do Git.
Após isso, se você rodar `git log`, verá algo como:

```
commit a3f1c9f (HEAD -> main)
Author: Seu Nome <email@exemplo.com>
Date:   Mon Aug 11 14:05 2025
    Mensagem descritiva
```

---

### 4.6 Enviar mudanças para o repositório remoto

```bash
git push origin main
```

📌 Publica as mudanças no GitHub (ou outro servidor Git).
Após o push, o código estará visível para todos no repositório remoto.

---

### 4.7 Baixar mudanças do repositório remoto

```bash
git pull origin main
```

📌 Atualiza seu código com as últimas mudanças feitas por outros colaboradores.

---

## 📂 5. Branches e Merges

### Criar uma branch

```bash
git branch nova-feature
```

📌 Cria uma nova linha de desenvolvimento **sem afetar a branch principal**.

### Trocar para outra branch

```bash
git checkout nova-feature
```

📌 Agora você está trabalhando nessa branch, e as mudanças não afetam a `main`.

### Criar e trocar de branch ao mesmo tempo

```bash
git checkout -b nova-feature
```

### Juntar branch com a principal

```bash
git checkout main
git merge nova-feature
```

📌 O conteúdo da `nova-feature` será integrado à `main`.

---

## 🔧 6. Comandos Úteis

| Comando            | Função                                |
| ------------------ | ------------------------------------- |
| `git log`          | Lista todos os commits                |
| `git diff`         | Mostra diferenças entre arquivos      |
| `git reset --hard` | Desfaz mudanças (cuidado!)            |
| `git stash`        | Guarda mudanças temporariamente       |
| `git remote -v`    | Lista repositórios remotos conectados |

---

## 💡 7. Boas Práticas

* Faça commits pequenos e descritivos.
* Use branches para novas funcionalidades.
* Sempre faça `git pull` antes de começar a trabalhar.
* Mantenha o repositório limpo (remova arquivos desnecessários).
* Utilize `.gitignore` para não rastrear arquivos temporários.

---

## 🔗 8. Recursos Úteis

* [Documentação oficial do Git](https://git-scm.com/doc)
* [Guia rápido GitHub](https://docs.github.com/pt)
* [Pro Git (livro gratuito)](https://git-scm.com/book/pt-br/v2)

---

Se quiser, eu posso **incluir exemplos visuais de antes e depois de cada comando** para mostrar **como os arquivos aparecem no Git** antes e depois do commit/push/pull.
Isso deixa o guia ainda mais prático e “de impacto” para quem está começando.

Quer que eu já faça essa versão com antes/depois visual?
