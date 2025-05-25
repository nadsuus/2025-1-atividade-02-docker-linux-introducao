# README - Atividade 02: Introdução a Linux usando Docker no Windows

Este repositório contém o relatório da **Atividade 02** da disciplina **Sistemas Operacionais (SO 2025.1)**, ministrada pelo Prof. Leonardo A. Minora, no IFRN - Campus Natal-Central.

---

## 1. Cabeçalho

* **Título da atividade**: Introdução a Linux usando Docker no Windows
* **Aluno**: *Nadson Santos Nascimento*
* **Data**: *25/05/2025*

---

## 2. Sumário

1. [Introdução](#introducao)
2. [Objetivo](#objetivo)
3. [Ferramentas e Pré-requisitos](#ferramentas-e-prerequisitos)
4. [Procedimentos e Prints](#procedimentos-e-prints)

   * 4.1 [Iniciar contêiner Fedora](#iniciar-conteiner-fedora)
   * 4.2 [Navegação básica](#navegacao-basica)
   * 4.3 [Manipulação de arquivos](#manipulacao-de-arquivos)
   * 4.4 [Gerenciamento de pacotes](#gerenciamento-de-pacotes)
   * 4.5 [Permissões de arquivos](#permissoes-de-arquivos)
   * 4.6 [Processos em execução](#processos-em-execucao)
   * 4.7 [Encerramento do contêiner](#encerramento-do-conteiner)
5. [Conclusão](#conclusao)

---

## 3. Introdução

Neste documento apresento o passo a passo das atividades práticas de introdução ao Linux, realizadas em um contêiner Docker baseado em Fedora. Cada seção contém prints de tela que comprovam a execução dos comandos solicitados.

---

## 4. Objetivo

O objetivo desta atividade é familiarizar-se com comandos básicos de sistemas Linux, através de um ambiente controlado em contêiner Docker. Ao final, o aluno deve demonstrar o domínio de operações de navegação, manipulação de arquivos, gerenciamento de pacotes e processos.

---

## 5. Ferramentas e Pré-requisitos

* **Docker** instalado no Windows (ou WSL + Docker).
* Acesso ao **PowerShell** ou **Prompt de Comando**.
* Imagem Docker: `fedora:latest`.

---

## 6. Procedimentos e Prints

### 6.1 Iniciar contêiner Fedora

```bash
docker run -it --name fedora-tutorial fedora:latest /bin/bash
```

> **Print 1:** Início do contêiner
>
> *Insira aqui o print da tela do terminal*

> `imagens/print1-iniciar-container.png`


---

### 6.2 Navegação básica

Comandos executados:

```bash
pwd
cd ~
ls
mkdir atividades
cd atividades
cd ..
```

> **Print 2:** Navegação e criação de diretório
>
> *Insira aqui o print  mostrando `pwd`, `ls` e `mkdir`*
> `imagens/print2-navegacao.png`

---

### 6.3 Manipulação de arquivos

Passos:

1. `touch arquivo1.txt`
2. `mv arquivo1.txt documento.txt`
3. `cd atividades`
4. `mkdir backup`
5. `cp ~/documento.txt backup/`
6. `rm ~/documento.txt`
7. `ls atividades/backup/`

> **Print 3:** Criação, cópia e remoção de arquivos
>
> *Insira aqui o print mostrando `mv`, `cp` e `rm`*
> `imagens/print3-manipulacao-arquivos.png`

---

### 6.4 Gerenciamento de pacotes

Comandos Fedora (`dnf`):

```bash
dnf update -y
dnf install nano -y
nano --version
dnf remove nano -y
```

> **Print 4:** Instalação e remoção do nano
>
> *Insira aqui o print das saídas do `dnf install` e `dnf remove`*
> `imagens/print4-gerenciamento-pacotes.png`

---

### 6.5 Permissões de arquivos

Comandos:

```bash
touch script.sh
ls -l script.sh
chmod u+x script.sh
ls -l script.sh
```

> **Print 5:** Antes e depois do `chmod`
>
> *Insira aqui os prints das permissões antes e depois*
> `imagens/print5-permissoes.png`

---

### 6.6 Processos em execução

Passos:

```bash
ps aux
sleep 60 &
ps aux | grep sleep
kill <PID>
ps aux | grep sleep
```

> **Print 6:** Listagem de processos e encerramento
>
> *Insira aqui o print mostrando `ps aux`, `grep sleep` e `kill`*
> `imagens/print6-processos.png`

---

### 6.7 Encerramento do contêiner

```bash
exit
docker rm fedora-tutorial
```

> **Print 7:** Saída do contêiner e remoção
>
> *Insira aqui o print mostrando a remoção do contêiner*
> `imagens/print7-encerramento.png`

---

## 7. Conclusão

Neste relatório, executei os principais comandos básicos do Linux em um contêiner Fedora. Aprendi a navegar na hierarquia de diretórios, manipular arquivos, gerenciar pacotes, alterar permissões e controlar processos. Essas habilidades são fundamentais para o gerenciamento de sistemas Linux.

---

*Fim do README.md*
