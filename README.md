# Aula-exerc-cios-12-11-2024
Aula exercícios 12/11/2024
#!/bin/bash 




read -p "Insira o caminho do diretório: " dir_path



   
    echo "Conteúdo do diretório $dir_path:"
    ls -l


    if [[ ! -d "Backup" ]]; then
        mkdir Backup
        echo "'Backup' criado com sucesso."
    else
        echo "'Backup' já existe."
    fi

  
    mv *.txt Backup/ 2>/dev/null

    echo "Todos os ficheiros .txt foram movidos para o diretório 'Backup'."


tmsma@LAPTOP-2J4K537L MINGW64 ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
$ chmod +x organizar_diretorio.sh

tmsma@LAPTOP-2J4K537L MINGW64 ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
$ ./organizar_diretorio.sh
Insira o caminho do diretório: ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
Conteúdo do diretório ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta:
total 1998
-rwxr-xr-x 1 tmsma 197609      26 Oct 30 12:19  bash
-rwxr-xr-x 1 tmsma 197609     840 Nov  5 10:06 'bash  exercicios'
-rwxr-xr-x 1 tmsma 197609      47 Nov  5 12:33  bem_vindo.sh
-rw-r--r-- 1 tmsma 197609       0 Nov  5 10:40  calcular_imc.sh
-rw-r--r-- 1 tmsma 197609       0 Nov 12 11:07 'exercicio 1'
-rw-r--r-- 1 tmsma 197609 2029333 Oct 30 12:29  exercicios-aula1.pdf
-rwxr-xr-x 1 tmsma 197609      33 Nov  5 12:24  hello.sh
-rwxr-xr-x 1 tmsma 197609     302 Nov  6 11:05  listnumpares
-rwxr-xr-x 1 tmsma 197609     302 Nov  6 11:05  listnumpares.sh
-rw-r--r-- 1 tmsma 197609       0 Oct 30 12:34  nano
-rw-r--r-- 1 tmsma 197609       0 Nov  5 11:50  ola_mundo.sh
-rwxr-xr-x 1 tmsma 197609     610 Nov 12 11:13  organizar_diretorio.sh
-rwxr-xr-x 1 tmsma 197609     235 Nov  6 10:51  soma.sh
'Backup' criado com sucesso.
Todos os ficheiros .txt foram movidos para o diretório 'Backup'.

exercicio 2


#!/bin/bash


read -p "Insira o nome do ficheiro (com extensão): " filename

if [[ -f "$filename" ]]; then

    line_count=$(wc -l < "$filename")
    word_count=$(wc -w < "$filename")
    
 
    echo "Primeiras 5 linhas do ficheiro:"
    head -n 5 "$filename"
    

    echo -e "\nLinhas que contêm a palavra 'erro':"
    grep -i "erro" "$filename"  
    

    echo "Número total de palavras: $word_count"
else
    echo "O ficheiro especificado não foi encontrado."
fi

tmsma@LAPTOP-2J4K537L MINGW64 ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
$ chmod +x contar_linhas_palavras.sh

tmsma@LAPTOP-2J4K537L MINGW64 ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta



exercico 3

#!/bin/bash


read -p "Insira o nome do ficheiro para salvar a lista de processos: " filename


ps aux > "$filename"

echo "A lista de processos foi salva no ficheiro '$filename'."


tmsma@LAPTOP-2J4K537L MINGW64 ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
$ chmod +x listar_processos.sh

tmsma@LAPTOP-2J4K537L MINGW64 ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
$ ./listar_processos.sh
Insira o nome do ficheiro para salvar a lista de processos:  ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
./listar_processos.sh: line 7: ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta: No such file or directory
A lista de processos foi salva no ficheiro '~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta'.
$ ./contar_linhas_palavras.sh
Insira o nome do ficheiro (com extensão): ~/OneDrive/Ambiente de Trabalho/Citeform/Nova pasta
O ficheiro especificado não foi encontrado.



