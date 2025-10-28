

# Conversioni binarie

- Con *n* bit codifichiamo $2^n$ numeri nell'intervallo $[0; 2^n - 1]$
- Per convertire un numero naturale in binario si usa il metodo dei resti, dividendo il numero considerato per 2 fino ad arrivare allo 0/1: 

| dividendo | divisore | resto |
| :-------: | :------: | :---: |
|    19     |    2     |   1   |
|     9     |    2     |   1   |
|     4     |    2     |   0   |
|     2     |    2     |   0   |
|     1     |    2     |   1   |
|     0     |          |       |

- Formula per rappresentare il numero *N* in bit $=log2(N+1)$
- 