# Trabalho_SiSoP
Trabalho Sistemas Operacionais

VM
 - Gerencia de Memoria
Monitor
 - Gerenciador de Processos
    - Process Controll Block (PCB)


## Compile
> javac Sistema.java

## Run
> java Sistema

### Observações
Implementados um caso de teste para comprovar o funcionamento do gerenciamento de maemoria e paginacao. 
Há uma variável dentro da classe GM, ***busyFrameTest***, se true, ela seta todos os frames pares como ocupados. Isso permite visualizar a interpolação de paginacao.

Outra implementacao foi a variavel ***dynamicOverridePages***,se habilitada como true, permite que o programa durante sua execução faça alocação dinamica de paginas. Por exemplo, se o programa tem tamanho 16, são alocadas proporcionais paginas para 16 endereços. Caso ele solicite o endereco 20, não tera em sua paginas, neste caso, o programa faz alocação de um novo frama (procura pelos frames e aloca no primeiro livre (FirstFit)). Obs: Não há sobreescrita, é validado o frameLivre[]=true



## Terminal Commands
Funções solicitadas:
- **cria *NomeDoPrograma***: faz a alocação do processo no sistema. Retorna o Id do processo. Podem ser alocados varios processos simultaneamente
- **executa *id***: executa o id do processo alocado.
- **dump *id***: Exibe os informações do processo/PCB e frames de memoria
- **dumpM *0 1***: Exibe um dump das posicoes de memoria definidas por 0=inicio e 1=final
- **desaloca *id***: desaloca o processo. Remove-o da lista de processos. Os frames são liberados (FrameLivre[]=true), mas o conteúdo da posição não é limpo. PoréM, o frameLivre permite ser sobreescrito

Ex

*Cuidar sensetive case*

```
cria PA
executa 0
dump 0
dumpM 3 20
desaloca 0
```


Outras funções extras:

- **dumpAllFrames**: Exibe todos os frames da memoria, seu conteudo e seu estado de referencia a pagina algum processo (se ocupado, frameLivre=false)
- **dumpFrame *frame***: Exibe as informações do frame solicitado (conteudo e ocupação)
- **ps**: Exibe todos os processos carregados.
- **exit**: finaliza o sistema 
-  :(em branco) quebra de linha

Ex:

```
dumpAllFrames
dumpFrame 2
ps
exit
 
```
