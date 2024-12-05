# Proj-Sistema-Operacional-2
## Simulador de Sistema de Arquivos com Journaling
### Descrição do Projeto
Este projeto é um simulador de sistema de arquivos desenvolvido em Java. Ele simula operações básicas de um sistema de arquivos, como copiar, excluir, renomear arquivos, criar e remover diretórios, e listar conteúdo de diretórios. Além disso, o simulador implementa a técnica de Journaling, que registra todas as operações realizadas em um arquivo de log para garantir integridade e possibilitar recuperação em caso de falhas.

O projeto tem como objetivo fornecer insights sobre o funcionamento de sistemas de arquivos e demonstrar a importância do journaling em sistemas operacionais modernos.

### Funcionalidades
#### Operações Suportadas:

copy <origem> <destino>: Copia arquivos entre caminhos especificados. <br>
rm <arquivo>: Remove arquivos no sistema de arquivos. <br>
mkdir <diretório>: Cria um novo diretório. <br>
rmdir <diretório>: Remove um diretório e todo o seu conteúdo. <br>
rename <caminho_atual> <novo_caminho>: Renomeia arquivos ou diretórios. <br>
ls <diretório>: Lista arquivos e diretórios no caminho especificado. <br>
### Journaling:

Todas as operações realizadas são registradas em um arquivo de log chamado filesystem.journal, permitindo auditoria ou recuperação em caso de falha.
### Estrutura do Projeto
O projeto é organizado com as seguintes classes principais:

#### Main:

Classe principal do simulador. <br>
Lida com a entrada de comandos pelo usuário e executa as operações correspondentes. <br>
#### Métodos de Operação:

copyArchive: Copia arquivos. <br>
deleteArchive: Exclui arquivos. <br>
createDirectory: Cria diretórios. <br>
deleteDirectory: Remove diretórios e seu conteúdo. <br>
rename: Renomeia arquivos ou diretórios. <br>
listDirectory: Lista o conteúdo de um diretório. <br>
#### Journaling:

Registra todas as operações realizadas no arquivo filesystem.journal.
### Como Executar
#### Pré-requisitos:

Certifique-se de ter o Java JDK instalado na sua máquina. <br>
Adicione o javac e o java ao PATH do seu sistema. <br>
#### Compilação:

Compile o código-fonte com o seguinte comando: <br>
javac Main.java

#### Execução:

Execute o simulador com o comando: <br>
java Main

#### Uso:

Digite os comandos suportados diretamente no terminal para realizar operações. <br>
Exemplo: <br>
> mkdir test_folder <br>
> copy file.txt test_folder/file.txt <br>
> ls test_folder <br>

#### Sair:

Para encerrar o simulador, digite: <br>
exit

### Estrutura do Journaling
Todas as operações realizadas são registradas no arquivo filesystem.journal. Cada linha do arquivo contém o comando executado, os parâmetros fornecidos e a ordem em que foi realizado.

Exemplo de registro no arquivo de journaling: <br>

mkdir test_folder <br>
copy file.txt test_folder/file.txt <br>
rm file.txt <br>

### Resultados Esperados
Ao executar o simulador, espera-se que o usuário consiga: <br>

Realizar operações comuns de manipulação de arquivos e diretórios. <br>
Visualizar o registro de todas as operações realizadas no arquivo de journaling. <br>
Entender como funciona a implementação de journaling e sua importância para garantir a integridade do sistema de arquivos. <br>

### Tecnologias Utilizadas
#### Linguagem: Java
#### Bibliotecas:
java.nio.file: Para manipulação de arquivos e diretórios. <br>
java.io: Para leitura e gravação no arquivo de journaling. <br>
