#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>

typedef struct no {
    int codigo;
    char nome[20];
    struct no *next;
} no;

struct no *corrente, *auxiliar, *auxiliar2, *inicio;

void enterdata(){
printf("\nInforme o codigo:");
scanf("%d", &corrente->codigo);
printf("\nInforme o nome:");
scanf("%s", &corrente->nome);
system("pause");
system("cls");
}

void inserir(){
if(inicio == NULL){
    corrente = (no*)malloc(sizeof(no));
    auxiliar = corrente;
    inicio = corrente;
    corrente->next = NULL;
    enterdata();
    }
    else{
        auxiliar = inicio;
        while(auxiliar->next != NULL){
            auxiliar = auxiliar->next;
        }
    corrente = auxiliar;
    corrente = (no*)malloc(sizeof(no));
    auxiliar->next = corrente;
    corrente->next = NULL;
    auxiliar = corrente;
    enterdata();
    }
}

void buscaporcodigo(){

int codigobusca;
int achou = 0;

if(inicio == NULL){
    printf("Lista Vazia\n");
    system("pause");
    system("cls");
    return;
    }
    else{
        printf("Digite codigo para procurar\n");
        scanf("%d", &codigobusca);
        auxiliar = inicio;
            while(auxiliar){
                    if(auxiliar->codigo == codigobusca){
                        printf("Codigo encontrado\n");
                        printf("Codigo digitado:%d\n", auxiliar->codigo);
                        printf("Nome:%s\n", auxiliar->nome);
                        achou = 1;
                        system("pause");
                        system("cls");
                        break;
                        }
                        else{
                            auxiliar = auxiliar->next;
                            }
                        }
                    if(achou == 0){
                        printf("Registro nao consta na lista\n");
                        system("pause");
                        system("cls");
                        }
            }
}

void consultapornome(){

char busca[20];
int achou = 0;
int k = 0;

if(inicio == NULL){
    printf("Lista vazia\n");
    system("pause");
    system("cls");
    }
    else{
        printf("Informe o nome a ser consultado:\n");
        scanf("%s", &busca);
        auxiliar = inicio;
            while(auxiliar != NULL){
                    k++;
                    if(strcmp(busca, auxiliar->nome) == 0){
                        printf("Registro encontrado na posicao %d", k);
                        system("pause");
                        system("cls");
                        achou = 1;
                        break;
                        }
                        else{
                            auxiliar = auxiliar->next;
                            }
                        }
                    if(achou == 0){
                        printf("Registro nao consta na lista\n");
                        system("pause");
                        system("cls");
                        }
            }
}

void removerporcodigo(){

int codigoremove;
int achou = 0;

if(inicio == NULL){
    printf("Lista vazia\n");
    system("pause");
    system("cls");
    }
    else{
        printf("Digite o codigo que deseja remover:\n");
        scanf("%d", &codigoremove);
        auxiliar = inicio;
            while(auxiliar != NULL){
                if(inicio->codigo == codigoremove){
                    printf("Elemento removido\n");
                    inicio = auxiliar->next;
                    free(auxiliar);
                    achou = 1;
                    system("pause");
                    system("cls");
                    break;
                    }
                    else
                    {
                        if(auxiliar->codigo==codigoremove){
                            printf("Elemento removido\n");
                            corrente->next = auxiliar->next;
                            free(auxiliar);
                            achou = 1;
                            system("pause");
                            system("cls");
                            break;
                            }
                            else{
                                corrente = auxiliar;
                                auxiliar = auxiliar->next;
                                }
                }
}
    if(achou == 0){
        printf("Registro nao consta na lista");
        system("pause");
        system("cls");
        }
    }
}

void removerpornome(){

char nomeremove[20];
int achou = 0;

if(inicio == NULL){
    printf("Lista vazia\n");
    system("pause");
    system("cls");
    }
    else{
        printf("Digite o nome que deseja remover:\n");
        scanf("%s", &nomeremove);
        auxiliar = inicio;
            while(auxiliar != NULL){
                if(strcmp(nomeremove, inicio->nome) == 0){
                    printf("Elemento removido\n");
                    inicio = auxiliar->next;
                    free(auxiliar);
                    achou = 1;
                    system("pause");
                    system("cls");
                    break;
                    }
                    else{
                        if(strcmp(auxiliar->nome, nomeremove)==0){
                            printf("Elemento removido\n");
                            corrente->next = auxiliar->next;
                            free(auxiliar);
                            achou = 1;
                            system("pause");
                            system("cls");
                            break;
                            }
                            else{
                                corrente = auxiliar;
                                auxiliar = auxiliar->next;
                                }
                }
}
    if(achou == 0){
        printf("Registro nao consta na lista\n");
        system("pause");
        system("cls");
        }
    }
}

void exibirlista(){

int k = 0;

if(inicio == NULL){
    printf("Lista Vazia\n");
    system("pause");
    system("cls");
    }
    else{
        auxiliar = inicio;
        while(auxiliar != NULL){
            k++;
            printf("-----------------------------\n");
            printf("Nome[%d]:%s\n", k, auxiliar->nome);
            printf("Codigo[%d]:%d\n", k, auxiliar->codigo);
            printf("-----------------------------\n");
            auxiliar = auxiliar->next;
            }
        system("pause");
        system("cls");
        }
}

void classordem(){

int achou = 0;
corrente = (no*)malloc(sizeof(no));
enterdata();
auxiliar = inicio;

if(inicio == NULL){
    inicio = corrente;
    corrente->next = NULL;
    printf("Primeiro elemento da lista inserido com sucesso\n");
    system("pause");
    system("cls");
    achou = 1;
    }
else{
    if(strcmp(corrente->nome, auxiliar->nome)<0){
        corrente->next = auxiliar;
        inicio = corrente;
        achou = 1;
        printf("Elemento inserido com sucesso no comeco da lista\n");
        system("pause");
        system("cls");
        }
        else{
            auxiliar2 = auxiliar->next;
            while(auxiliar2 != NULL){
                if(strcmp(corrente->nome, auxiliar->nome)>= 0 && strcmp(corrente->nome, auxiliar2->nome)<= 0){
                    auxiliar->next = corrente;
                    corrente->next = auxiliar2;
                    printf("Elemento inserido com sucesso no meio da lista\n");
                    system("pause");
                    system("cls");
                    achou = 1;
                    break;
                    }
                    else{
                        auxiliar = auxiliar->next;
                        auxiliar2 = auxiliar2->next;
                        }
                }
        }
}

if(achou == 0 && strcmp(corrente->nome, auxiliar->nome)>= 0){
    auxiliar->next = corrente;
    corrente->next = NULL;
    achou = 1;
    printf("Elemento inserido no final da lista\n");
    system("pause");
    system("cls");
    }
}

int main(){

corrente = NULL;
inicio = NULL;
auxiliar = NULL;
int opcao;

do{
    printf("Digite sua opcao\n");
    printf("[1] Inserir Dados\n");
    printf("[2] Procurar Dados por Codigo\n");
    printf("[3] Procurar Dados por Nome\n");
    printf("[4] Remover Dados por Codigo\n");
    printf("[5] Remover Dados por Nome\n");
    printf("[6] Exibir Lista\n");
    printf("[7] Classificar Lista\n");
    printf("[8] Sair\n");
    scanf("%d", &opcao);
        switch(opcao){
            case 1:
                inserir();
                break;
            case 2:
                buscaporcodigo();
                break;
            case 3:
                consultapornome();
                break;
            case 4:
                removerporcodigo();
                break;
            case 5:
                removerpornome();
                break;
            case 6:
                exibirlista();
                break;
            case 7:
                classordem();
                break;
            case 8:
                break;
            default:
                break;
}
}while(opcao != 8);
}
