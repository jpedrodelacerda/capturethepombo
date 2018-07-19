## bandit12 -> 13

Chave no arquivo data.txt que é um hexdump comprimido repetidas vezes.
> Recomendado copiar o arquivo para uma pasta temporária, aqui usarei /tmp/gras

```
$ mkdir /tmp/gras
$ cp data.txt /tmp/gras; cd /tmp/gras
```

Reverter o dump do data.txt e descobrir o tipo de arquivo que foi comprimido:
```
$ xxd -r data.txt data1
$ file data1
data0: gzip compressed data, was "data2.bin", last modified: Thu Dec 28 13:34:36 2017, max compression, from Unix
$ mv data1 data1.gz
```

Agora o processo é descomprimir os arquivos repetidamente:
  - se for um arquivo gzip:
  ```
    $ gzip -d arquivo.gz
  ```
ou
  ```
  $ zcat arquivo > novoarquivo
  ```
- se for um arquivo bzip:
  ```
    $ bzip2 -d arquivo.bz2
  ```
- se for um arquivo tar:
  ```
  $ tar xf arquivo
  ```

Finalmente um arquivo ASCII text:
```
$ file data9.bin 
data9.bin: ASCII text
$ cat data9.bin
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

##### Chave:
> _8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL_

