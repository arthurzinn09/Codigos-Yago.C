// 1.c código do professor
#include &lt;stdio.h&gt;
int main() {
    int a,b;
    printf("Insira o Numero 1: \n");
    scanf("%d", &a);
    printf("Insira o Numero 2: \n");
    scanf("%d", &b);

    printf("Soma: %d", a+b);
    return 0;
}

// 2.c código do professor
#include <stdio.h>

int main() {
    int a = 1;

    while(a != 0){
    printf("Insira um numero: \n");
    scanf("%d", &a);
    if(a % 2 == 0){
        printf("%d eh par!\n", a);
    }else{
        printf("%d eh impar!\n",a);
    }
    }
}

// 4.c
#include <stdio.h>

int main () {
  int n1,n2,n3,n4,n5,n6;
printf("Mostre o numero 1: ");
  scanf("%d", &n1);
  printf("Mostre o numero 2: ");
    scanf("%d", &n2);
  printf("Mostre o numero 3: ");
    scanf("%d", &n3);
  printf("Mostre o numero 4: ");
    scanf("%d", &n4);
  printf("Mostre o numero 5: ");
    scanf("%d", &n5);
  printf("Mostre o numero 6: ");
    scanf("%d", &n6);
  printf("A média desses seis números é: %d", (n1+n2+n3+n4+n5+n6)/6);
  return 0;}

// 5.c 
#include <stdio.h>

int main() {
    int ano;

    
    printf("Digite um ano: ");
    scanf("%d", &ano);

    
    if ((ano % 4 == 0 && ano % 100 != 0) || (ano % 400 == 0)) {
        printf("%d é um ano bissexto.\n", ano);
    } else {
        printf("%d não é um ano bissexto.\n", ano);
    }

    return 0;
}


// 7.c
#include <stdio.h>

int main() {
    int a, b, c;

    printf("Digite três números: ");
    scanf("%d %d %d", &a, &b, &c);

    int maior = a;

    if (b > maior) maior = b;
    if (c > maior) maior = c;

    printf("O maior número é: %d\n", maior);
    return 0;
}

// 8.c
#include <stdio.h>
#include <math.h>

int main() {
    double num;

    printf("Digite um número: ");
    scanf("%lf", &num);

    if (num < 0) {
        printf("Número negativo não tem raiz real.\n");
    } else {
        printf("A raiz quadrada de %.2f é %.2f\n", num, sqrt(num));
    }

    return 0;
}

// 10.c
  #include <stdio.h>

  int main() {
      float a, b, c;

      printf("Digite os três lados do triângulo: ");
      scanf("%f %f %f", &a, &b, &c);

      if (a + b > c && a + c > b && b + c > a) {
          if (a == b && b == c)
              printf("Triângulo equilátero.\n");
          else if (a == b || a == c || b == c)
              printf("Triângulo isósceles.\n");
          else
              printf("Triângulo escaleno.\n");
      } else {
          printf("Os valores não formam um triângulo.\n");
      }

      return 0;
  }


// 13.c
#include <stdio.h>

int main() {
    int n;
    float nota, peso, somaNotas = 0, somaPesos = 0;

    printf("Quantas notas você quer inserir? ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        printf("Nota %d: ", i);
        scanf("%f", &nota);
        printf("Peso da nota %d: ", i);
        scanf("%f", &peso);

        somaNotas += nota * peso;
        somaPesos += peso;
    }

    if (somaPesos != 0)
        printf("Média ponderada = %.2f\n", somaNotas / somaPesos);
    else
        printf("Soma dos pesos é zero. Não é possível calcular.\n");

    return 0;
}


// 25.c
#include <stdio.h>

int main() {
    float fahrenheit, celsius;

    printf("Digite a temperatura em Fahrenheit: ");
    scanf("%f", &fahrenheit);

    celsius = (fahrenheit - 32) * 5 / 9;

    printf("Temperatura em Celsius: %.2f\n", celsius);
    return 0;
}


// 27.c
#include <stdio.h>

int main() {
    float preco, novoPreco;

    printf("Digite o preço do produto: ");
    scanf("%f", &preco);

    if (preco < 100)
        novoPreco = preco * 1.10;
    else
        novoPreco = preco * 1.20;

    printf("Preço reajustado: R$ %.2f\n", novoPreco);
    return 0;
}



// 28.c

#include <stdio.h>

int main() {
float total, valorFinal, valorParcela;
int opcao, parcelas;
printf("Informe o total gasto: R$ ");
  scanf("%f", &total);
printf("\nOpcoes de pagamento:\n");
printf("1 - A vista com 10%% de desconto \n----------------------------------------\n");
printf("2 - Em duas vezes (sem juros)\n----------------------------------------\n");
printf("3 - De 3 ate 10 vezes com 3%% de juros ao mes (para compras acima de R$100,00\n----------------------------------------\n");
printf("Escolha a opcao desejada: \n----------------------------------------\n");
scanf("%d", &opcao);

if (opcao == 1) {
valorFinal = total * 0.90;
printf("Valor com 10%% de desconto: R$ %.2f\n----------------------------------------\n", valorFinal);
} else if (opcao == 2) {
valorParcela = total / 2;
printf("2 parcelas de R$ %.2f (sem juros)\n----------------------------------------\n", valorParcela);
} else if (opcao == 3) {
if (total <= 100) {
printf("Essa opcao so esta disponivel para compras acima de R$100,00.\n----------------------------------------\n");
} else {
printf("Digite o numero de parcelas (de 3 a 10): \n----------------------------------------\n");
scanf("%d", &parcelas);

if (parcelas >= 3 && parcelas <= 10) {
valorFinal = total;
for (int i = 0; i < parcelas; i++) {
valorFinal += valorFinal * 0.03;
}
valorParcela = valorFinal / parcelas;
printf(" Ficaram %d parcelas (com juros) de R$ %.2f\n", parcelas, valorParcela);
printf("Total com juros: R$ %.2f\n", valorFinal);
} else {
printf("Numero de parcelas invalido. Deve ser de 3 a 10.\n");
}
}
} else {
printf("Opcao invalida.\n");
}
return 0;
}
