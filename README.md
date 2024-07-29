# Técnicas do If... Else

Existem duas técnicas que são sempre bem vindas no If Else, uma é concatenar as condições em um único If e a outra é utilizar uma única linha de resposta. Abaixo explicarei um pouco mais, como e quando implementar cada uma delas.

## If Else sem Chaves {}

A técnica de utilizar apenas uma única linha consiste em descartar as ```{}``` após a condição. Entretanto, ela pode ser utilizada somente quando existe um único resultado, ou seja, podemos transformar o exemplo:

```
if ( 2+2 == 4 ){
    document.write("A soma é verdadeira");
}else{
    document.write("A soma é falsa");
}
```

Em:

```
if ( 2+2 == 4 )
    document.write("A soma é verdadeira");
else
    document.write("A soma é falsa");
```

Com essa técnica ainda podemos reduzir o código para ocupar duas linhas de forma clara e eficiente, ex:

```
if ( 2+2 == 4 ) document.write("A soma é verdadeira");
else document.write("A soma é falsa");
```

## Concatenando IFs

Para as estruturas de condição If Else e Operador Ternário é possível juntar duas ou mais condições em um único If. Por exemplo, quando temos o trecho "verifique se um número é ímpar e positivo", pode ser resolvido da seguinte forma:

```
let numeroImparPositivo = 5;

if (numeroImparPositivo % 2 != 0 && numeroImparPositivo >= 0){
    document.write(`O número ${numeroImparPositivo} é ímpar e positivo`);

}else {
    document.write(`O número ${numeroImparPositivo} não é ímpar e positivo`);
}
```

Destrinchando a linha 3, temos:
- A expressão ```numeroImparPositivo % 2 != 0```, que resultará no resultado falso, e ```numeroImparPositivo >= 0```, que resultará em verdadeiro. Entre essas duas expressões há o operador de igualdade ```&&```, que compara um resultado com o outro.

O operador de igualdade && do ECMA Script retorna um resultado verdadeiro só e somente quando ambos os resultados são iguais, ou seja, quando ambos os resultados são verdadeiros ou falsos. Como por exemplo:

-> O número 5 é positivo ```e (&&)``` ímpar, mas não é par ```e (&&)``` negativo.

- Nas seguintes linhas, caso o resultado seja verdadeiro é impresso o texto "O número ```5``` é ímpar e positivo".
- Caso contrário, imprime "O número ```5``` não é ímpar e positivo".

### Utilizando Ambas as Técnicas do If

Utilizando ambas as técnias de abreviação, o código acima pode ser expresso da seguinte forma:

```
let numeroImparPositivo = 5;
if (numeroImparPositivo % 2 != 0 && numeroImparPositivo >= 0) document.write(`O número ${numeroImparPositivo} é ímpar e positivo`);
else document.write(`O número ${numeroImparPositivo} não é ímpar e positivo`);
```

## If... If... Else

Dentre as várias formas de se utilizar o If Else, quando se tem mais de uma verificação é possível utilizar-se da abertura de vários Ifs com apenas um fechamento, por exemplo:

```
let numero = 5;

if (numero % 2 == 0) document.write(`O número ${numero} é par`);
if (numero >= 0) document.write(`O número ${numero} é positivo`);
else document.write(`O número ${numero} é impar`);
```

Por outro lado este método não é tão eficiente quando busca-se obter mais de um resultado.