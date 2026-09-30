## <font color="#ff0000">While</font>
```run-c
#include <stdio.h>

int main() {
    int contador = 1;

    while (contador <= 5) {
        printf("%d\n", contador);
        contador++;
    }

    return 0;
}
```

## <font color="#ff0000">do while</font>
```run-c
#include <stdio.h>

int main() {
    int contador = 1;

    do {
        printf("%d\n", contador);
        contador++;
    } while (contador <= 5);

    return 0;
}
```

## <font color="#ff0000">for</font>
```run-c
#include <stdio.h>

int main() {
    for (int i = 1; i <= 5; i++) {
        printf("%d\n", i);
    }

    return 0;
}
```