/*1. Realice una función que lea un archivo de TEXTO con la información de los deportistas.
2. Realice una función que reciba los deportistas leídos y calcule e imprima el número de medallas por
deporte.

Nota: Dentro del código existe un arreglo que contiene los nombres de todos los deportes que existen en el archivo.

char deporte[6][30] = {"Natación", "Atletismo", "Ciclismo", "Gimnasia", "Equitacion", "Esgrima"};

Encontrará el código en el siguiente repositorio https://github.com/mirnabotello/EDI-parcial3:

1.  Deberá hacer fork del repositorio
2.  Subir la solución desde su cuenta de github.
3.  Deberá enviar la liga a su repositorio. */

#include <stdio.h>
#include <string.h>

typedef struct {
    char nombre[40];
    char pais[25];
}DatosPersonales;

typedef struct{
    DatosPersonales datos;
    char deporte[30];
    int numMedallas;
}Deportista;

void captura(int N, Deportista *deportistas, ¿archi?);

int main()
{
    Deportista deportistas[100];

    int N;

    archi= fopen("deportistas.txt", "r");

    printf("dame el numero de deportistas\n");
    scanf("%d", &N);

    void captura(N, &deportistas, ¿archi?);
    void medallas(N, deportistas);
    return 0;
}

void captura(int N, Deportista *deportistas, ¿archi?)
{
    int i;

    for(i=0; i<N; i++)
    {
        fscanf("archi", "%s", &deportistas[i]->datos.nombre);
        fscanf("archi", "%s", &deportistas[i]->datos.pais);
        fscanf("archi", "%s", &deportistas[i]->deporte);
        fscanf("archi", "%d", &deportistas[i]->numMedallas);
    }
}

void medallas(int N; Deportista deportistas)
{
    char deporte[6][30] = {"Natación", "Atletismo", "Ciclismo", "Gimnasia", "Equitacion", "Esgrima"};
    int medallas[6];
    int i;

    for(i=0; i<6; i++)
    {
        medallas[i]=0;
    }

    for(i=0; i<N; i++)
    {
        for(int j=0; j<6; j++)
        {
            if(strcmp(deportistas[i].deporte, deporte[j])
                medallas[j] = medallas[j] + deportistas[i].numMedallas;
        }
    }

    for(i=0; i<6; i++)
    {
        printf("El numero total de medallas obtenidas en %s es %d", deporte[i], medallas[i]);
    }
}
