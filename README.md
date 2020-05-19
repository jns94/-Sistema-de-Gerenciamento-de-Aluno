# -Sistema-de-Gerenciamento-de-Aluno
#include<stdio.h>
#include<stdlib.h>
struct Aluno{
  char codigo[6];
  char nome[30];
  char disciplina[20];
  float aval1;
  float aval2;
  float aval3;
  float media;
  char conceito[1];
  }alunos[4];
  float calcular_media(float aval1 , float aval2 , float aval3){
    float media = 3/(aval1+aval2+aval3);
   }
   int main (){
   int pos_cadastradas[4];
   int index = 0;
   int pos;
   int opcao;
   
   do{
    printf("1.Cadastrar | 2.Lançar Nota | 3.Alterar Nota | 4.Mostrar Relatório dos Estudantes | 0.Sair:");
    scanf("%d",&opcao);
    switch(opcao){
      case 1:
        pos = 0;
        printf("\nPosicao(de 0 a 4):");
        scanf("%d",&pos);
        if (pos <= 4){
        fflush(stdin);
        printf("Código: ");
        gets(alunos[pos].codigo);
        printf("Nome: ");
        gets(alunos[pos].nome);
        printf("Disciplina: ");
        gets(alunos[pos].disciplina);
        printf("Avaliação 1: ");
        scanf("%f", &alunos[pos].aval1);
        pos_cadastradas[index] = pos;
        index++;
        break;
        pritnf("\n1.Cadastrar | 2.Lançar Nota | 3.Alterar Nota | 4.Mostrar Relatório dos Estudantes | 0.Sair:");
    scanf("%d",&opcao);
    }else{
      printf("Opcao invalida, fechando algoritmo...");
                    exit(-1);
    }
    case 2:
     pos = 0;
        printf("\nPosicao(de 0 a 4):");
        scanf("%d",&pos);
        if (pos <= 4){
        fflush(stdin);
        printf("Código: ");
        gets(alunos[pos].codigo);
        printf("Nome: ");
        gets(alunos[pos].nome);
        printf("Disciplina: ");
        gets(alunos[pos].disciplina);
        printf("Avaliação 2: ");
        scanf("%f", &alunos[pos].aval2);
        pos_cadastradas[index] = pos;
        index++;
        break;
        pritnf("\n1.Cadastrar | 2.Lançar Nota | 3.Alterar Nota | 4.Mostrar Relatório dos Estudantes | 0.Sair:");
    scanf("%d",&opcao);
    }else{
      printf("Opcao invalida, fechando algoritmo...");
                    exit(-1);
}                    
      case 3:
       pos = 0;
        printf("\nPosicao(de 0 a 4):");
        scanf("%d",&pos);
        if (pos <= 4){
        fflush(stdin);
        printf("Código: ");
        gets(alunos[pos].codigo);
        printf("Nome: ");
        gets(alunos[pos].nome);
        printf("Disciplina: ");
        gets(alunos[pos].disciplina);
        printf("Avaliação 3: ");
        scanf("%f", &alunos[pos].aval3);
        alunos[pos].media = calcular_media(alunos[pos].aval1,alunos[pos].aval2,alunos[pos].aval3);
        pos_cadastradas[index] = pos;
        index++;
       break;
        pritnf("\n1.Cadastrar | 2.Lançar Nota | 3.Alterar Nota | 4.Mostrar Relatório dos Estudantes | 0.Sair:");
        scanf("%d",&opcao);
    }else{
        printf("Opcao invalida, fechando algoritmo...");
                    exit(-1);
}                    
    case 4:
        for(int i = 0; i < index; i++){
                    printf("\nCódigo:%s",alunos[pos_cadastradas[i]].codigo);
                    printf("\nNome:%s",alunos[pos_cadastradas[i]].nome);
                    printf("\nAvalição 1:%f",alunos[pos_cadastradas[i]].aval1);
                    printf("\nAvalição 2:%f",alunos[pos_cadastradas[i]].aval2);
                    printf("\nAvalição 3:%f",alunos[pos_cadastradas[i]].aval3);
                    printf("\nMédia:%f",alunos[pos_cadastradas[i]].media);                    
}
    break;
        pritnf("\n1.Cadastrar | 2.Lançar Nota | 3.Alterar Nota | 4.Mostrar Relatório dos Estudantes | 0.Sair:");
        scanf("%d",&opcao);    
    case 5:
        exit(0);    
    case 6:
        for(int i = 0; i < index; i++){
        printf("\nMédia:%f",alunos[pos_cadastradas[i]].media);
}
    break;
        pritnf("\n1.Cadastrar | 2.Lançar Nota | 3.Alterar Nota | 4.Mostrar Relatório dos Estudantes | 0.Sair:");
        scanf("%d",&opcao);
    default:
        printf("Opcao invalida, fechando algoritmo...");
                 exit(-1);
   }  
 }while(opcao!= 0);
 system("PAUSE");
}
