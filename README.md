# Trabalho_SiSoP
Trabalho Sistemas Operacionais

VM
 - Gerencia de Memoria
Monitor
 - Gerenciador de Processos
    - Process Controle Block (PCB)


## Compile
javac Sistema.java

## Run
java Sistema

### Observações

## Terminal Commands
Funções solicitadas:
- **cria *NomeDoPrograma***: faz a alocao do processo no sistema. Retorna o Id do processo. Podem ser alocados varios processos simultaneamente
- **executa *id***: executa o id do processo alocado.
- **dump *id***: Exibe os informações do processo/PCB e frames de memoria
- **dumpM *0 1***: Exibe um dump das posicoes de memoria definidas por 0=inicio e 1=final
- **desaloca *id***: desaloca o process. Remove-o da lista de processos. Os frames são liberados, mas o conteúdo da posição não é limpo. Poré, o frameLivre permite ser sobreescrito
Cuidar sensetive case:

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
dumpFrame 2
```
