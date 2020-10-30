# Biblioteca console.h

Biblioteca com funções para manipulação do console.

## Características

- Linguagem: **C e C++**
- Compilador: **MinGW (GCC)**
- Autor: **desconhecido**
- Edição: **David Gomesh**

## Sumário

- [Funções](#funções)
  - [gotoxy()](#função-gotoxy)
  - [textcolor()](#função-textcolor)
  - [backgroundcolor()](#função-backgroundcolor)
- [Como usar](#como-usar)
- [Cores disponíveis](#cores-disponíveis)
- [Definição de COLORS](#definição-de-colors)
- [Inclusões duplicadas](#inclusões-duplicadas)
- [Bibliotecas utilizadas](#bibliotecas-utilizadas)
- [Variáveis importantes](#variáveis-importantes)
- [Tipos importantes](#tipos-importantes)
- [Exemplos](#exemplos)

## Funções

### Função gotoxy

```c
int gotoxy(DWORD x, DWORD y);
```

**Funcionalidade:** Aponta o cursor para determinada posição do console.

**Retorno:**

- **1:** caso a função consiga apontar para posição indicada.
- **0:** caso a função não consiga apontar para posição indicada.

**Obs 1.:** ***x*** representa colunas e ***y*** representa linhas.

**Obs 2.:** ***[DWORD](#Tipos-importantes)*** é o tipo ***unsigned long***.

**Obs 3.:** As linhas e colunas devem ser contadas a partir de **1**. A função automaticamente decrementará o número passado.

---

### Função textcolor

```c
void textcolor(int color);
```

**Funcionalidade:** Altera a cor a ser usado nos próximos textos.

**Retorno:** sem retorno.

**Obs 1.:** Pode-se passar um número inteiro de ***0 a 15***, ou usar os elementos da estrutura **enum** definida como [COLORS](#cores-disponíveis).

*[Veja a estrutura COLORS](#definição-de-colors)*

---

### Função backgroundcolor

```c
void backgroundcolor(int color);
```

**Funcionalidade:** Altera a cor do fundo a ser usado nos próximos textos.

**Retorno:** sem retorno.

**Obs 1.:** Pode-se passar um número inteiro de ***0 a 15***, ou usar os elementos da estrutura **enum** definida como [COLORS](#cores-disponíveis).

*[Veja a estrutura COLORS](#definição-de-colors)*

## Como usar

### Colocar a biblioteca na pasta do projeto

| ![Demonstração do arquivo console.h na pasta do projeto](https://user-images.githubusercontent.com/65545355/97735820-9a019900-1ab9-11eb-8e29-f5e9edd03214.png "Demonstração do arquivo console.h na pasta do projeto") |
|-|
| *Demonstração do arquivo console.h na pasta do projeto* |

### Fazer a inclusão da biblioteca no projeto

| ![Demonstração da inclusão do arquivo console.h no projeto](https://user-images.githubusercontent.com/65545355/97736130-febcf380-1ab9-11eb-9529-5f2ef3024411.png "Demonstração da inclusão do arquivo console.h no projeto") |
|-|
| *Demonstração da inclusão do arquivo console.h no projeto* |

**Feito isso, as funções estão prontas para uso.**

## Cores disponíveis

Cor | Valor decimal | Valor hexadecimal | Disponível como | Visualização
:-:|:-:|:-:|:-:|:-:
Preto | 0 | 0 | **BLACK** | <img src="https://user-images.githubusercontent.com/65545355/97728920-e4324c80-1ab0-11eb-977a-86beb5ae55f0.png" width="50" heigth="25" title="Preto" alt="Demonstração da cor Preto">
Azul | 1 | 1 | **BLUE** | <img src="https://user-images.githubusercontent.com/65545355/97728947-eac0c400-1ab0-11eb-8fdf-e1a117c8fcd4.png" width="50" height="25" title="Azul" alt="Demostração da cor Azul">
Verde | 2 | 2 | **GREEN** | <img src="https://user-images.githubusercontent.com/65545355/97728995-f7451c80-1ab0-11eb-8a31-bf084e1c756c.png" width="50" heigth="25" title="Verde" alt="Demonstração da cor Verde">
Verde-água | 3 | 3 | **CYAN** | <img src="https://user-images.githubusercontent.com/65545355/97729022-fe6c2a80-1ab0-11eb-9b27-3b47c84081ee.png" width="50" heigth="25" title="Verde-água" alt="Demonstração da cor Verde-água">
Vermelho | 4 | 4 | **RED** | <img src="https://user-images.githubusercontent.com/65545355/97729030-02984800-1ab1-11eb-9a84-7ab2039b7e06.png" width="50" heigth="25" title="Vermelho" alt="Demonstração da cor Vermelho">
Roxo | 5 | 5 | **MAGENTA** | <img src="https://user-images.githubusercontent.com/65545355/97729043-06c46580-1ab1-11eb-9a05-428d8cb6aa01.png" width="50" heigth="25" title="Roxo" alt="Demonstração da cor Roxo">
Amarelo | 6 | 6 | **BROWN** | <img src="https://user-images.githubusercontent.com/65545355/97729057-0af08300-1ab1-11eb-85ad-0e1e2aacb7d3.png" width="50" heigth="25" title="Amarelo" alt="Demonstração da cor Amarelo">
Branco | 7 | 7 | **LIGHTGRAY** | <img src="https://user-images.githubusercontent.com/65545355/97729079-10e66400-1ab1-11eb-87d0-5cc9e607e21b.png" width="50" heigth="25" title="Branco" alt="Demonstração da cor Branco">
Cinza | 8 | 8 | **DARKGRAY** | <img src="https://user-images.githubusercontent.com/65545355/97729086-1479eb00-1ab1-11eb-9e92-13b2545af943.png" width="50" heigth="25" title="Cinza" alt="Demonstração da cor Cinza">
Azul claro | 9 | 9 | **LIGHTBLUE** | <img src="https://user-images.githubusercontent.com/65545355/97729099-1774db80-1ab1-11eb-818a-e5960d1fc363.png" width="50" heigth="25" title="Azul claro" alt="Demonstração da cor Azul claro">
Verde claro | 10 | A | **LIGHTGREEN** | <img src="https://user-images.githubusercontent.com/65545355/97729115-1ba0f900-1ab1-11eb-8112-b0c1c6ba3076.png" width="50" heigth="25" title="Verde claro" alt="Demonstração da cor Verde claro">
Verde-água claro | 11 | B | **LIGHTCYAN** | <img src="https://user-images.githubusercontent.com/65545355/97729136-1f348000-1ab1-11eb-9afa-c1f51d4bda0a.png" width="50" heigth="25" title="Verde-água claro" alt="Demonstração da cor Verde-água claro">
Vermelho claro | 12 | C | **LIGHTRED** | <img src="https://user-images.githubusercontent.com/65545355/97729142-22c80700-1ab1-11eb-8ab3-ac7aa0dfd572.png" width="50" heigth="25" title="Vermelho claro" alt="Demonstração da cor Vermelho claro">
Lilás | 13 | D | **LIGHTMAGENTA** | <img src="https://user-images.githubusercontent.com/65545355/97729156-278cbb00-1ab1-11eb-8d61-bf20a28bfa62.png" width="50" heigth="25" title="Lilás" alt="Demonstração da cor Lilás">
Amarelo claro | 14 | E | **YELLOW** | <img src="https://user-images.githubusercontent.com/65545355/97729169-2c516f00-1ab1-11eb-859f-b2c4eca394ca.png" width="50" heigth="25" title="Amarelo claro" alt="Demonstração da cor Amarelo claro">
Branco brilhante | 15 | F | **WHITE** | <img src="https://user-images.githubusercontent.com/65545355/97729176-307d8c80-1ab1-11eb-918a-a37a0ac51c1a.png" width="50" heigth="25" title="Branco brilhante" alt="Demonstração da cor Branco brilhante">

</br>

### Definição de COLORS

```c
typedef enum{
    BLACK,
    BLUE,
    GREEN,
    CYAN,
    RED,
    MAGENTA,
    BROWN,
    LIGHTGRAY,
    DARKGRAY,
    LIGHTBLUE,
    LIGHTGREEN,
    LIGHTCYAN,
    LIGHTRED,
    LIGHTMAGENTA,
    YELLOW,
    WHITE
} COLORS;
```

## Inclusões duplicadas

A fim de evitar inclusões duplicadas, foram adicionadas as seguintes condições:

```c
#ifndef CONSOLE_H_INCLUDED
#define CONSOLE_H_INCLUDED

/*
    Implementação
*/

#endif /* CONSOLE_H_INCLUDED */
```

## Bibliotecas utilizadas

- ***windows.h***

## Variáveis importantes

- **__BACKGROUND:** guarda a cor de fundo;
- **__FOREGROUND:** guarda a cor do texto;

## Tipos importantes

- **DWORD:** unsigned long.
- **COLORS:** enum.

## Exemplos

## Usando a textcolor e backgroundcolor

| ![Exemplo de código usando as funções textcolor() e backgroundcolor()](https://user-images.githubusercontent.com/65545355/97738988-ed75e600-1abd-11eb-84e3-4d1b0c618524.png "Exemplo de código usando as funções textcolor() e backgroundcolor()") |
|-|
| *Exemplo de código usando as funções textcolor() e backgroundcolor()* |

| ![A saída será com as cores que foram informadas](https://user-images.githubusercontent.com/65545355/97739518-b3591400-1abe-11eb-8621-323361e11be1.png "A saída será com as cores que foram informadas") |
|-|
| *A saída será com as cores que foram informadas* |

## Usando a gotoxy

| ![Exemplo de código usando a função gotoxy()](https://user-images.githubusercontent.com/65545355/97739874-34181000-1abf-11eb-91f9-342bf7fd6260.png "Exemplo de código usando a função gotoxy()") |
|-|
| *Exemplo de código usando a função gotoxy()* |

| ![A saída será nas posições que foram informadas](https://user-images.githubusercontent.com/65545355/97740012-5f9afa80-1abf-11eb-99ca-4056f58aa414.png "A saída será nas posições que foram informadas") |
|-|
| *A saída será nas posições que foram informadas* |