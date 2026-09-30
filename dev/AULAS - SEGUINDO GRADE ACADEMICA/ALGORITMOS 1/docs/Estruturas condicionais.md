## <font color="#ff0000">if</font>
```run-c
#include <stdio.h>

int main() {
    int idade = 20;

    if (idade >= 18) {
        printf("Maior de idade\n");
    }

    return 0;
}
```

## <font color="#ff0000">else</font>
```run-c
#include <stdio.h>

int main() {
    int idade = 16;

    if (idade >= 18) {
        printf("Maior de idade\n");
    } else {
        printf("Menor de idade\n");
    }

    return 0;
}
```

## <font color="#ff0000">else if </font>
```run-c
#include <stdio.h>

int main() {
    int nota = 7;

    if (nota >= 9) {
        printf("Excelente\n");
    } else if (nota >= 7) {
        printf("Aprovado\n");
    } else if (nota >= 5) {
        printf("Recuperacao\n");
    } else {
        printf("Reprovado\n");
    }

    return 0;
}
```


## <font color="#ff0000">switch case</font>
```run-c
#include <stdio.h>

int main() {
    int opcao = 2;

    switch (opcao) {
        case 1:
            printf("Cadastrar\n");
            break;

        case 2:
            printf("Consultar\n");
            break;

        case 3:
            printf("Sair\n");
            break;

        default:
            printf("Opcao invalida\n");
    }

    return 0;
}
```
