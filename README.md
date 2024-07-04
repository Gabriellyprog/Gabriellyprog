- 👋 Hi, I’m @Gabriellyprog
- 👀 I’m interested in aprender sobre software 
- 🌱 I’m currently learning engenharia de software 
- 📫 How to reach me, me chame no meu e-mail @alvesgabrielly401@gmail.com 
- 😄 Pronouns: ela/dela
<!---
Gabriellyprog/Gabriellyprog is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <stdio.h>
#include <string.h>

#define MAX_NAMES 100
#define MAX_LENGTH 100

void bubbleSort(char arr[][MAX_LENGTH], int n) {
    int i, j;
    char temp[MAX_LENGTH];

    for (i = 0; i < n-1; i++) {
        for (j = 0; j < n-i-1; j++) {
            if (strcmp(arr[j], arr[j+1]) > 0) {
                // Trocar as strings
                strcpy(temp, arr[j]);
                strcpy(arr[j], arr[j+1]);
                strcpy(arr[j+1], temp);
            }
        }
    }
}

int main() {
    char names[MAX_NAMES][MAX_LENGTH];
    int n, i;

    printf("Quantos nomes você quer inserir? ");
    scanf("%d", &n);
    getchar(); // Limpar o buffer de entrada

    printf("Digite os nomes:\n");
    for (i = 0; i < n; i++) {
        fgets(names[i], MAX_LENGTH, stdin);
        names[i][strcspn(names[i], "\n")] = 0; // Remover a nova linha
    }

    bubbleSort(names, n);

    printf("\nNomes ordenados:\n");
    for (i = 0; i < n; i++) {
        printf("%s\n", names[i]);
    }

    return 0;
}
Aqui está um programa onde ajuda a retirar todos os nomes inseridos em orde alfabética 
