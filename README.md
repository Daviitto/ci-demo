# CI Demo – GitHub Actions

## 1. Descrição do projeto

Este projeto demonstra a criação de um **pipeline simples de Continuous Integration (CI)** utilizando **GitHub Actions**.
O pipeline é executado automaticamente sempre que ocorre um **push no repositório**, simulando um processo básico de automação usado em ambientes DevOps.

---

## 2. Objetivo da atividade

O objetivo desta atividade é demonstrar como configurar um **workflow de integração contínua** no GitHub.
Através desse pipeline é possível automatizar tarefas que normalmente seriam feitas manualmente, como executar scripts ou validar mudanças no código.

---

## 3. Estrutura do projeto

O projeto possui a seguinte estrutura de arquivos:

```
.github/workflows/ci.yml
README.md
```

**Descrição dos arquivos:**

* **.github/workflows/ci.yml** → Arquivo responsável por definir o workflow do GitHub Actions.
* **README.md** → Documento que descreve o projeto, sua estrutura e funcionamento.

---

## 4. Explicação do workflow

Arquivo `ci.yml`:

```yaml
name: CI Example

on: [push]

jobs:
  first-job:
    runs-on: ubuntu-latest

    steps:
      - name: Print message
        run: echo "Pipeline executado com sucesso!"
```

**Explicação de cada parte:**

* **name: CI Example**
  Define o nome do workflow que aparecerá na aba **Actions** do GitHub.

* **on: [push]**
  Define o evento que dispara o pipeline. Neste caso, o workflow será executado sempre que houver um **push** no repositório.

* **jobs**
  Define os trabalhos (jobs) que serão executados pelo pipeline.

* **first-job**
  Nome do job que será executado.

* **runs-on: ubuntu-latest**
  Define que o job será executado em uma máquina virtual com **Ubuntu**, fornecida pelo GitHub.

* **steps**
  Lista de etapas que o job executará.

* **name: Print message**
  Nome da etapa que será exibida durante a execução.

* **run: echo "Pipeline executado com sucesso!"**
  Comando que será executado no terminal do runner.

---

## 5. Fluxo do pipeline

O fluxo de execução do pipeline ocorre da seguinte forma:

```
Push no GitHub
      ↓
Disparo automático do GitHub Actions
      ↓
Criação de um ambiente Ubuntu
      ↓
Execução do workflow
      ↓
Execução do comando echo
      ↓
Exibição do resultado na aba Actions
```

---

## 6. Resultado da execução

Quando um **push** é realizado no repositório, o GitHub Actions inicia automaticamente o pipeline.

Durante a execução:

1. O GitHub cria um **runner Ubuntu**.
2. O workflow definido no arquivo `ci.yml` é carregado.
3. O job **first-job** é executado.
4. O comando `echo` imprime a mensagem:

```
Pipeline executado com sucesso!
```
