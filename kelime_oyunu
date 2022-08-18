#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <time.h>
#include <conio.h>

void delay(int a)
{
    int süre;
    int ekleme;
    int i;
    süre=a*100000000;
    for (int i = 1; i < süre; i++)
    {
        ekleme*=i;
        ekleme++;
        ekleme++;
    }
}

int main() {
    //TANIMLAMALAR
    char hazirmisin,tahminedilenharf,kelimeyitahmin,varmisinyokmusun;
    char kelimeler[][15]={"marmara","universite","mekatronik","muhendislik","birinci","sinif"};
    char kelimetahmini[]={};
    char gizlikelimedizisi[]={};
    int kelimedizisininindisi,kelimedizisininboyutu;
    int tahminascii,kelimeascii,denemehakki,sonkarsilastirma;
    int m=0;

    srand(time(NULL));



//-------------------BAŞLANGIÇ------------------------\\

    printf("**********KELIME OYUNU**********\n");
    printf("   Kelime Oyununa Hosgeldiniz :)\n");



    baslangic:{
    printf("\nOyuna Baslamak Icin Lutfen 'E/e' Karakterlerinden Bir Tanesini Giriniz: ");
    scanf(" %c",&hazirmisin);
    if(hazirmisin=='e' || hazirmisin=='E'){


//KELİME BELİRLENMESİ
        kelimedizisininindisi = (rand() % 6);
        kelimedizisininboyutu = strlen(kelimeler[kelimedizisininindisi]);
        memset(gizlikelimedizisi, '*', kelimedizisininboyutu);
        denemehakki=kelimedizisininboyutu;

//--------------------------------\\



        //GİRİŞ METİNLERİ//
        printf("\n");
        printf("Oyun Basliyor Hazir Olun \n\n");
        printf("Kelimeniz Belirleniyor.\n");
        delay(3);
        printf("...\n");
        delay(4);
        printf("Kelimeniz Bulundu  :)\n");
        delay(1.5);

        printf("Kelimeniz = ");
        for (int i = 0; i < kelimedizisininboyutu; ++i) {
            printf("%c", gizlikelimedizisi[i]);
        }
        printf("\t (Kelimeniz %d Harfli)\n", kelimedizisininboyutu);

        printf("Simdi Harf Bulma Zamani Harf Bulma Menusune Aktariliyorsunuz ... \n");
        delay(1.5);
        printf("\n");

        printf("!!! Harf Tahmin Zamani !!!\n");
        do {
            printf("\nDeneme Hakkiniz = %d",denemehakki);
            printf("\nLutfen Bir Harf Giriniz = ");
            scanf(" %c", &tahminedilenharf);
            tahminascii = tahminedilenharf;

            if(tahminedilenharf=='x'){
                goto bitis;
            }
            int u=0;
            printf("\n");
            for (int i = 0; i < kelimedizisininboyutu; i++) {
                kelimeascii = kelimeler[kelimedizisininindisi][i];
                if (tahminascii == kelimeascii) {
                    printf("!!! Bravo Tahmin Edilen Harf Kelimenin %d. Harfi !!!\n", i + 1);
                    gizlikelimedizisi[i] = tahminedilenharf;
                    u=u+1;
                }
            }
            if(u==0)printf("\n Maalesef Girdiginiz Harf Kelimede Yok :( \n");
            denemehakki--;
            printf("\n");
            printf("Kelimenin Son Hali : ");
            for (int i = 0; i < kelimedizisininboyutu; ++i) {
                printf("%c", gizlikelimedizisi[i]);
            }

            int p;
            p=memcmp(gizlikelimedizisi,kelimeler[kelimedizisininindisi],kelimedizisininboyutu);
            if ( p==0)
                goto songidis;


            m =m+1;
            printf("\n");
            if(denemehakki>0)  printf("\nKelimeyi Tahmin Etmek Istiyorsaniz 'x' Basiniz \n");

        }while(0<denemehakki);

        bitis:{
        if(denemehakki<=0)printf("\nDeneme Hakkiniz Bitti Simdi Kelimeyi Tahmin Etme Vakti\n");
        printf("\n Lutfen Kelime Tahmininizi Girin = ");
        scanf("%s",&kelimetahmini);
        sonkarsilastirma= strcmp(kelimetahmini,kelimeler[kelimedizisininindisi]);
            songidis:{
        if(sonkarsilastirma==0){
            printf("\n !!!!TEBRIKLER KELIMEYI DOGRU BILDINIZ!!!! \n");
            printf("Bir Daha Oynamaya Ne Dersin ???\n");
        } else{
            printf("\n :( MAALESEF KELIMEYI BULAMADINIZ :( \n");
            printf("Dogru Kelime = ");
                printf("%s",kelimeler[kelimedizisininindisi]);
            printf("\n\n");
            printf("Bir Daha Denemeye Ne Dersin ???\n\n");
        }

        printf("Varsan 'D'/'d' ye bas :)\n");
        printf("Eger Oyundan Cikmak Istiyorsan 'C'/'c' ye bas :)\n\n");
    };
    }
        tekrar : {
        printf("O Zaman Var Misin Yok Musun?? =\n");
        scanf(" %c",&varmisinyokmusun);

        if(varmisinyokmusun == 'd' || varmisinyokmusun == 'D')
            goto baslangic;
        else if (varmisinyokmusun == 'C' || varmisinyokmusun == 'c')
            goto son;
        else{
            printf("Gecersiz Tus Lutfen Birdaha Deneyin\n");
            goto tekrar;
        }

    }

    }else{
        printf("\n !!!!!Yanlis Karakter Girdiniz !!!!! \n");
        printf("Lutfen Gecerli Bir Tuslama Yapiniz\n");
        goto baslangic;
    }
    son:{
    printf("\n OYUNU OYNADIGIN ICIN COK TESEKKUR EDERIZ TEKRAR BEKLERIZ :)\n");
};

}
}
