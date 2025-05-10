

# Atividade 02 - Introdução ao Linux usando Docker no Windows

**Nome:** Robson Alves de Alencastro  
**Disciplina:** Sistemas Operacionais (TADS - IFRN CNAT)  
**Professor:** Leonardo A. Minora  
**Data:** 09/05/2025

---

## Introdução

O propósito da atividade é proporcionar uma introdução prática ao sistema operacional Linux, utilizando um contai ner Docker com a imagem do Fedora. Executando comandos básicos de terminal, manipulação de arquivos, permissões, gerenciamento de pacotes e processos em execução, buscando entender melhor o funcionamento do Linux.

---

## Relato das Atividades

---

### Navegação Básica
![navegacao_basica](https://github.com/user-attachments/assets/b78b4aaf-50a0-46b8-bb79-9a9a7aade4dd)

A introdução consistiu na criação de um container a partir de uma imagem Linux. Durante esse processo, foi possível identificar o diretório inicial do ambiente, bem como utilizar comandos de navegação para explorar a hierarquia de diretórios do sistema de arquivos. Foram realizadas operações como a criação de um novo diretório, entrada e saída de diretórios, demonstrando na prática o funcionamento dos comandos de manipulação de diretórios e a estrutura básica do sistema dentro de um contêiner Linux.

---
### Manipulação de Arquivos
![manipulacao_arquivos](https://github.com/user-attachments/assets/539d0343-1bf1-4b59-9753-93d5f6bd16f6)

Nesta segunda etapa, foi realizada a navegação ao diretório home (cd ~), seguida da confirmação do diretório atual com pwd. Nesse local, foi criado um novo arquivo utilizando o comando touch, introduzindo o conceito de criação de arquivos no Linux, sem abordar ainda sua edição. Em seguida, o arquivo foi renomeado com o comando mv, apresentando um novo recurso de manipulação de arquivos.

Retornando ao diretório criado anteriormente (atividades), foi criada uma nova subpasta chamada backup. Utilizando o comando cp, o arquivo previamente criado foi copiado para essa nova pasta. Após a cópia, o arquivo original foi removido com o comando rm, e a integridade da cópia foi confirmada ao acessar o diretório backup e verificar sua presença.

Essa segunda parte permitiu a familiarização com comandos essenciais relacionados ao gerenciamento de arquivos no Linux: criação, renomeação, cópia e exclusão.

---

### Gerenciamento de Pacotes
![install_remove_dnf_nano](https://github.com/user-attachments/assets/2d7edc98-4798-4b1b-aa8f-7e132a299b33)

Neste ponto, foi utilizado o comando dnf update para atualizar a lista de pacotes disponíveis no sistema, garantindo que os dados estejam recentes. Em seguida, procedemos com a  instalação do editor de texto nano utilizando o comando dnf install nano. Após a instalação, a versão do editor foi verificada com nano --version, confirmando o sucesso da operação. Por fim, o pacote foi removido com dnf remove nano, demonstrando o ciclo completo de instalação e desinstalação de softwares no sistema.

Esta etapa é fundamental para reforçar o conceito de que o Linux adota uma abordagem em que diversos recursos e utilitários não vêm instalados por padrão, sendo responsabilidade do usuário instalar, configurar, equando necessário, remover esses componentes.

---

### Permissões de Usuário
![permissoes_arquivos](https://github.com/user-attachments/assets/a72509f3-63af-4e0a-bb82-7bcd67cca2bd)

Nesta fase foi criado um novo arquivo com a extensão .sh utilizando o comando touch, já utilizado anteriormente. Em seguida, o comando chmod foi utilizado para conceder permissão de execução ao proprietário do arquivo. Especificamente, a sintaxe chmod u+x nome_do_arquivo.sh foi utilizada:

chmod é o comando responsável por modificar permissões de arquivos:

* u refere-se ao usuário proprietário (user);

* +x adiciona a permissão de execução (execute);

* nome_do_arquivo.sh indica o target da modificação.

As permissões do arquivo foram verificadas com ls -l, permitindo observar o que foi modificado.

Essa etapa serviu como introdução ao controle de permissões no Linux, um conceito essencial para a administração de sistemas e segurança de arquivos.

---

### Processos em Andamento
![processos_andamento](https://github.com/user-attachments/assets/812c4afa-d75d-4369-9820-e99a21d4368a)

Foi necessário utilizar o comando ps, responsável por listar os processos em execução. Como o comando não estava disponível por padrão na imagem do container, foi preciso instalá-lo utilizando o gerenciador de pacotes dnf.

Com o ps disponível, foi possível listar os processos ativos na hora. Em seguida, foi utilizado o comando sleep com o operador &, iniciando um processo em segundo plano. Foi possível visualizar esse processocom o ps e posteriormente encerrá-lo com o comando kill, utilizando seu PID . Após o encerramento, a ausência do processo foi confirmada chamando o ps novamente.

 Vale salientar que a execução em um container Docker permitiu praticar esses comandos de forma sem impactar o sistema operacional real.

 ---

 ### Finalização do Container Docker
![encerrar](https://github.com/user-attachments/assets/65a117a5-6ced-4394-a7f6-d8c5675aac00)

Por fim, a aplicação foi encerrada e o container Docker de teste apagado com o comando docker rm.

---

### Considerações Finais

* O que foi aprendido?

  Ao longo da atividade, aprofundei meus conhecimentos sobre o sistema Linux, especialmente nos conceitos de diretórios, comandos fundamentais e a sintaxe utilizada no terminal. Fui introduzido a conceitos como permissões de arquivos, execução de processos em segundo plano e uso de comandos como ps, kill, chmod, touch e outros. Além disso, tive meu primeiro contato com o dnf, que é a ferramenta responsável pelo gerenciamento de pacotes no Fedora. Essa base prática contribuiu para entender melhor o funcionamento do sistema de modo geral.

* Dificuldades

  Não encontrei muitas dificuldades durante a realização da atividade, pois segui o passo a passo proposto pelo professor. Cometi alguns pequenos erros devido à falta de familiaridade com a sintaxe dos comandos, mas nada que impedisse o andamento da atividade.






 











