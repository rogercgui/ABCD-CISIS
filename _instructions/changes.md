### 5.4.02

1.  lw(0)
2.  na proc R: nome,mfn onde : indica pathdo db de entrada
3.  criação dos diretórios lindG lingG4 ffiG ffiG4

```
lindG : mstxl = 2G ... 512G
lingG4: mstxl = 2G ... 512G ate' 256 * 16 M mfns 0xFFFFFFFF
```

---

### 5.4.pre04 - 20/08/2008

Standard extended database size becomes 32 gigabytes.

---

5.4.pre05 - 12/09/2008

Bugfix regarding the conversion from mstxl to shift

bug de `/r/n`

in the message: `GET HTTP`

Adjusting CICONF2 build parameters of the mak as per AOT guidance.

---

### 5.4.pre06 - 01/10/2008

Alguns aplicativos exigiram alteração do parâmetro CICONF2

Alteração da estrutura de diretórios de saída dos aplicativos para  
\--- utl  
\--- windows  
\--- linux

correcao de bug de formato (mfn) em windows

Inicio da modificação dos fontes do aplicativo crunchif

Adalberto acrescentou parâmetro (jdi) no mx. 

Alterados os fontes  (12/12/2008)

*   mxaot.c 
*   mxrun.c
*    w2ov3.c

Inclusão no menu do mx:

`jdi[/]==`  
`/lines:1000/width:60`  
`/tab:2/occ:30`  
`/wmin:0.05/vmin:0.05/nmin:2`  
`/sort:{w|v|n}{1|2|3}`  
`/top:10`  
`/55`  
`/show`

---

### 5.4.pre07 - 12/03/2009

Alteração do menu do mx de:

```
seq[/1m]=|
xml[/1m]=|
```

para:

```

seq[/1m]=[]|
list={./|
}|
xml[/1m]=,|
```

Alteração do menu do mx de:

`Gload[/][/nonl][/xml][/socket][/head][={|}]`

para:  
`Gload[/][/nonl][/xml][/socket][/head][={||dir=}]`

Alteração do menu do mx de:

`prolog|pft|epilog={|@} [lw={|0}]`

para:

`prolog|pft|epilog={|@} [lw={|0}] [pftout=]`

Correção da importação de arquivo marc para isis e o processo inverso

See https://web.archive.org/web/20100212050244/http://www.itsmarc.com/crs/auth0669.htm

```
            bytes 00-04 - Logical record length
            byte  05    - Record status
            byte  06    - Type of record
            bytes 07-08 - Undefined
            byte  09    - Character coding scheme
            byte  10    - Indicator count
            byte  11    - Subfield code length
            bytes 12-16 - Base address of data
            byte  17    - Encoding level
            bytes 18-19 - Undefined
            bytes 20-23 - Entry map   
```

Na importação via mx, supondo o uso do parâmetro isotag1=4000, serão mostrados os campos:

```
4005 - Record status
4009 - Character coding scheme
4017 - Encoding level
```

Na exportação via mx, todos os parâmetros do líder serão os padrões da norma, mas caso se deseje alterá-los deve-se criar os campos seguintes com o parâmetro  
outisotag1. Supondo o uso do parâmetro outisotag1=4000 normalmente devem existir no registro os campos:

*   Record status, 
*   Character coding scheme 
*   Encoding level,  

sendo que os dois últimos raramente serão alterados do valor padrão.

Um exemplo onde se importa e exporta um arquivo em formato marc via mx pode ser visto abaixo:

---

### 5.4.pre07

```
/utl/linux/isis/mx iso=marc=marc08.sample.bin isotag1=4000
outiso=marc=x.iso outisotag1=4000 now -all
```

Onde: `diff marc08.sample.bin x.iso` deve ser vazio.

---

### 5.4.pre08 - 12/03/2009

Alteração no arquivo _ciupd.c_. 

Onde estava:

```
#define PROCG 1
#if PROCG
#include "ciupg.c"
#endif /* PROCG */
```

ficou:

```
#ifndef PROCG
#define PROCG 1
#endif /* PROCG /
#if PROCG
#include "ciupg.c"
#endif / PROCG */
```

Geracao a pedido do Marcelo do aplicativo genqlf

---

### 5.5.pre02 - 14/10/2009

Correção de bug na indexação com a versão lindG4 - INFX - (ciifl.c ciifl.h ciiflh.c)  
Aumento de área de buffer (REPLYSIZE) em _serw.c_  
Correção do bug do parâmetro _what_ no _mx_

---

### 5.52 - 19/04/2010

Correção do bug do jdi em mxaot.c

---

### 5.53 - 24/05/2010

Correção do bug do jdi em mxaot.c (verificação se pesos no registro utilizado pelo parâmetro jdi= no mx estão ordenados)  
Correção do bug da função _Gmarx_ em _ciupdmarx.c_

---

### 5.6 - 08/11/2010

Correção do bug de não se gerar master com `mstxl=6` na versao FFIG4  
Alteração do código para compilação em máquinas 64 bits (parâmetros de sscanf) e do script de geração para as versões 32 e 64 bits.  
Geração das versões lind512G4 e ffi512G4.

---

### 5.7a - 17/08/2011

Alteração nos fontes dos aplicativos wtrig1 e wtrig2.  
Só define PACKED2 se for GCC  
Criação das categorias FFI1660 e isisG4 de aplicativos

---

### 5.7b - 07/05/2012

*   wxis - mudança da versão de 7.1e para 7.1f - alteração do tamanho de buffer nas versões nao FFI para permitir a indexação de registros com 32 kbytes.
*   Criação do sabor ffiG\_1024K-256 (nome temporário) com tamanho máximo padrão de registro de 1GB, tamanho de master ate 64GB, chaves ate 256 caracteres.
*   Apresentação do aviso de 64bits no bunner de todos os aplicativos.
*   Alteração da url dos aplicativos no copyright dos aplicativos.
*   Alteração do tipo de LONGX para _time\_t_ nos parâmetros das funções time() e localtime().
*   Alteração da permissão de escrita dos arquivos **mst** e **xrf** passando de 644 para 664 (pessoas do grupo passam a poder alterar os mesmos).
*   Criação do sabor ffiG4\_4 que e o mesmo do ffiG4 mas com registros com tamanho máximo padrão de 4 gigabytes.

---

### 5.7c - 18/06/2012

Bug corrigido na função _fmt\_load\_next\_occ_ onde na versão 64 bits a função strcpy apresentava comportamento diferente da versão 32 bits.

---

### 5.7d - 14/02/2013

Inseridas as modificações dos fontes feitas pelo Ricardo Piva para a inclusão do processamento de registros em formato UTF-8.

---

### 5.7e - xx/xx/2014

---

### 5.7f - 13/01/2015

Bug corrigido na função _recgizmo_. Antes o comprimento máximo do registro tinha que ser de 6 dígitos, agora passou a 8 dígitos.  
`'H 00000000 '`
