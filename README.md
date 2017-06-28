# Registro
#include <stdio.h>
int main(void){
    struct{
    int dd;
    int mm;
    int aaaa;
    }TU,TUTU;

    int f,g,N1,N2, N3;

    scanf("%d/%d/%d",&TU.dd, &TU.mm, &TU.aaaa);
     scanf("%d/%d/%d",&TUTU.dd, &TUTU.mm, &TUTU.aaaa);

    if(TU.mm<=2){
        TU.aaaa = TU.aaaa - 1;
        TU.mm = TU.mm + 13;
    }else{
        TU.mm = TU.mm + 1;
}
    if(TUTU.mm<=2){
        TUTU.aaaa = TUTU.aaaa - 1;
        TUTU.mm = TUTU.mm + 13;
    }else{
        TUTU.mm = TUTU.mm + 1;
}


    N1 = (1461*TU.aaaa)/4 + (153*TU.mm)/5 + TU.dd;

    N2 = (1461*TUTU.aaaa)/4 + (153*TUTU.mm)/5 + TUTU.dd;

    N3 = N1-N2;
    if(N3<0)
        N3*=-1;

        printf("Quantidade de dias: %d\n", N3);



return 0;
}
