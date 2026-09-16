---*---
Contexto e Objetivos: 
Criação do Google Notebook LM para estudar e obter respostas objetivas sobre uso e administração sistemas Linux.
---*---
Curadoria de Fontes:
https://www.inf.ufpr.br/cursos/ci055/linux.pdf
https://ribafs.github.io/down/livros/servidoreslinux.pdf
https://files.oxavi.com/ebooks/linux/Mastering-Ubuntu-Server.pdf
---*---
Engenharia de Prompts e "Cicatrizes":
Chat:
Pergunta:
Me liste 10 comandos mais uteis no ubuntu server
Resposta:
Com base no material do seu caderno, aqui estão **10 dos comandos mais úteis e essenciais** para administrar um **Ubuntu Server**:

1. **apt** **(Advanced Package Tool)**: É o gestor de pacotes do Ubuntu Server. É utilizado para atualizar o índice de repositórios (`apt update`), atualizar pacotes instalados (`apt upgrade`) e instalar ou remover programas (`apt install` / `apt remove`)[1].
2. **systemctl**: Comando do `systemd` para gerir serviços (*units* ou *daemons*) no servidor. Permite verificar o estado (`systemctl status`), iniciar (`start`), parar (`stop`), reiniciar (`restart`) e configurar serviços para arrancarem automaticamente com o sistema (`enable`)[8].
3. **ls**: Lista o conteúdo e diretórios do sistema. Quando combinado com parâmetros como `-l` ou `-lh`, apresenta informações detalhadas como permissões, proprietário, data de alteração e tamanho dos ficheiros em formato legível[13].
4. **cd**: Comando de navegação utilizado para mudar de diretório e deslocar-se pela hierarquia do sistema de ficheiros[13].
5. **cp** **/** **mv**: O `cp` faz a cópia de ficheiros e diretórios (exigindo a opção `-r` para incluir subdiretórios de forma recursiva)[21], enquanto o `mv` permite mover ou renomear ficheiros e pastas[25].
6. **df** **/** **du**: O `df -h` apresenta uma visão geral do espaço livre e ocupado nos volumes e partições montadas[28]. O `du -h` analisa o consumo de espaço de diretórios e ficheiros específicos para identificar o que está a ocupar espaço em disco[30].
7. **ip**: Ferramenta moderna da suite `iproute2` para visualizar e gerir interfaces de rede. Permite consultar os endereços IP associados (`ip addr show` ou `ip a`) e alterar o estado de placas de rede (`ip link set`)[33].
8. **ps** **/** **htop**: O `ps` (ex.: `ps aux`) lista os processos em execução e os seus PIDs[37], enquanto o `htop` fornece um painel gráfico interativo no terminal para monitorizar a utilização do CPU, memória e consumo de recursos em tempo real[41].
9. **grep**: Filtra e pesquisa por padrões de texto específicos dentro de ficheiros ou na saída gerada por outros comandos através do uso de *pipes* (`|`)[44].
10. **chmod** **/** **chown**: O `chmod` é utilizado para alterar as permissões de acesso (leitura `r`, escrita `w` e execução `x`) de utilizadores, grupos e outros[51], enquanto o `chown` altera a propriedade (*owner*) do utilizador ou grupo sobre um ficheiro ou diretório[53].

💡 Quer que eu detalhe a sintaxe e exemplos de utilização de algum destes comandos em específico?
-----
Pergunta:
Como combinar comandos?
Resposta:
No Linux, existem três formas principais de combinar ou encadear comandos na linha de comandos: através do **pipe** (`|`), do operador lógico **&amp;&amp;** e do **ponto e vírgula** (`;`)[1].

### 1\. Usando o Pipe (`|`)

O operador **pipe** (a barra vertical `|`) pega na saída padrão de um comando e envia-a diretamente como entrada para o comando seguinte[1][4]. Isto permite criar sequências (*pipelines*) onde vários comandos processam dados em cadeia[5][6].

* **ls | sort**: Lista o conteúdo de uma pasta e envia esse texto para o comando `sort` ordená-lo[7].
* **dpkg -l | grep spotify**: Lista os pacotes de software do sistema e passa essa lista para o `grep` filtrar apenas as linhas que contêm "spotify"[8].
* **fortune | calcei | lolcat**: Encadeia três comandos em sequência, passando o texto gerado pelo `fortune` para o `calcei` e, por fim, para o `lolcat`[5].

### 2\. Usando o operador `&amp;&amp;` (E lógico)

O operador **&amp;&amp;** serve para executar o segundo comando **apenas se o primeiro comando for executado com sucesso**[2][10]. Se o primeiro comando falhar ou encontrar um erro, a sequência é interrompida[2][11].

* **sudo apt update &amp;&amp; sudo apt install apache2**: Executa a atualização dos repositórios e, caso esta conclua sem erros, inicia a instalação do pacote[2].

### 3\. Usando o Ponto e Vírgula (`;`)

O **ponto e vírgula (** **;** **)** permite separar e executar múltiplos comandos em sequência, **independentemente de o comando anterior ter tido sucesso ou ter falhado**[3].

* **sudo apt update; sudo apt install apache2**: O terminal executa a atualização e passa imediatamente para a instalação, independentemente do resultado do primeiro comando[3].
-----
Pergunta:
Como resolver problemas?
Resposta:
A resolução de problemas no Linux envolve uma abordagem metódica para identificar e corrigir falhas no sistema:

* **Investigar o problema de forma organizada**: Trate a resolução de falhas como uma investigação, eliminando hipóteses uma a uma e sem entrar em pânico, utilizando cópias de segurança de configurações anteriores como referência[1].
* **Consultar os manuais do sistema**: Utilize o comando **man
-----

Conclusão: Apesar de ser bem poluído o chat, não tive problemas com os resultados. Ficou bem explicativo e me deu ideia de usar o Gemini Notebook para colocar configurações e estruturas que tenho no trabalho e usar como consulta e analise.
---*---

Resumos estruturados do assunto:
Fiz um infografico.
<img width="2752" height="1536" alt="Guia_de_Produtividade_no_Terminal" src="https://github.com/user-attachments/assets/82bf35c1-31d3-4107-a25c-52e0e1c6d67d" />
Um resumo podcast de administração dos servidores:

Um glossário com os principais conceitos aprendidos;
Um conjunto de prompts reutilizáveis que possam apoiar futuras revisões sobre o tema.
