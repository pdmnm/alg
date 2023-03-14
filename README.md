#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define TAM1 4
#define TAM2 5

int main()
{
    int matriz[4][5];
    int quantidadePar = 0, quantidadeImpar = 0;
    int i, j;

    srand(time(NULL));

    //Prenchendo a Matriz
    for (i = 0; i < TAM1; i++) {
        for (j = 0; j< TAM2; j++) {
                matriz[i][j] = rand() % 300; //
        }
    }
    //Descobrindo os numeros pares e impares
    for (i = 0; i < TAM1; i++) {
        for (j = 0; j< TAM2; j++) {
            if (matriz[i][j] % 2 == 0) {
             quantidadePar++;
        }
            else {
                quantidadeImpar++;
                 }
           }
        }
    //exibindo a Matriz
    for (i = 0; i < TAM1; i++) {
        for (j = 0; j < TAM2; j++) {
            printf("%4d", matriz[i][j]);
        }
        printf("\n");

    }
    printf("\nA quantidade de pares e: %d" , quantidadePar);
    printf("\nA quantidade de Impares e: %d", quantidadeImpar);
    return 0;
}
