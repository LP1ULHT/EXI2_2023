**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**

*Linguagens de Programação I*

# Exercício Individual 2 - Trabalhos de Pintura
>Na resolução deste exercício deve ser utilizada a Linguagem de Programação C. Para além da correta implementação dos requisitos, tenha em conta os seguintes aspetos:
>- O código apresentado deve ser bem indentado. 
>- O código deve compilar sem erros ou *warnings* utilizando o *gcc* com as seguintes flags:
>- `-g -Wvla -Wall -Wpedantic -Wextra -Wdeclaration-after-statement`
>- Tenha em atenção os nomes dados das variáveis, para que sejam indicadores daquilo que as mesmas vão conter.
>- O trabalho deve ser desenvolvido e submetido de forma individual.

>Este exercício deverá ser submetido na plataforma Pandora até às 23h59 de dia 16 de Abril e será contabilizado para a nota final da unidade curricular de acordo com os critérios disponibilizados na página da disciplina, concretamente nos slides da primeira aula.

>Todos os trabalhos serão comparados utilizando um sistema de detecção de plágio.


## Contexto
 Suponha que uma equipa de pintores pretende pintar as paredes de um edifício. Estas paredes estão divididas em secções de iguais dimenções, identificadas através de números inteiros. Por exemplo, se uma paredes tivesse 10 secções, as secções 2, 3 e 4 poderiam ser atribuídas a um pintor, enquanto que outro poderia ficar com as secções 8 e 9. A forma de indicar estas esta atribuição no caderno de encargos seria a seguinte:
```
2-4,8-9
```
Por outras palavras, a cada pintor é atribuído um conjunto de secções. Atenção: a um pintor pode ser atribuída apenas uma secção, através de uma atribuição desta forma: `9-9`.

Como forma de agilizar o trabalho a equipa de pintores decide-se dividir em pares, duas pessoas a pintar dois conjuntos de secções torna o serviço mais rápido ainda que o número de pessoas por secção seja o mesmo. Estas atribuições são geradas por um programa que gera um ficheiro com este formato:
```
3-4,5-6
2-3,1-5
3-8,4-6
5-9,1-4
7-8,4-7
```
 Ao começarem a comparar as atribuíções com as do seu par, os pintores percebem que algumas das atribuições se sobrepõem, ou seja, existiria trabalho duplicado.
 
## Descrição

 Para tentar encontrar rapidamente quantos pares de atribuições têm trabalho duplicado os pintores precisam que os alunos escrevam um programa em C, que lê da consola estes pares. No exemplo cada par tem apenas um dígito para simplificar o exemplo, contudo, **há edifícios enormes, com IDs de paredes com valores muito, muito grandes, mas sempre positivos**.

 Para terminar o programa basta o pintor parar de inserir pares de números com o formato definido, não sendo necessário usar um comando de saída. Por outras palavras qualquer introdução de dados fora de formato faz parar o programa. Em seguida o programa deverá mostrar a contabilização de quantos pares:
 1. Têm Sobreposição (overlaped), por exemplo, `2-3,3-5`
 2. Quantos estão totalmente contidos (included) no outro conjunto, por exemplo `4-9, 6-8` ou `2-3,1-6`
 3. Número total de trabalhos atribuídos

Veja-se o formato esperado na consola:
 ```
intervals included 5
intervals overlaped 12
total cases 19
 ```

## Honestidade Académica

Nesta disciplina, espera-se que cada aluno siga os mais altos padrões de honestidade académica. Trabalhos que sejam identificados como cópias serão anulados e os alunos envolvidos terão nota zero - quer tenham copiado, quer tenham deixado copiar.
Para evitar situações deste género, recomendamos aos alunos que nunca partilhem ou mostrem o seu código.
A decisão sobre se um trabalho é uma cópia cabe exclusivamente aos docentes da unidade curricular.
Os alunos são encorajados a discutir os problemas com outros alunos mas não deverão, no entanto, copiar códigos, documentação e relatórios de outros alunos. Em nenhuma circunstância deverão partilhar os seus próprios códigos, documentação e relatórios. De facto, não devem sequer deixar códigos, documentação e relatórios em computadores de uso partilhado.
