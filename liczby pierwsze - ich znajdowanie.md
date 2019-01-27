# Java---programy-dzialajace

// Co robi program?: znajduje liczby pierwsze 	z przedzialu od 0 do 7919. (czyli 1000 liczb znajdzie)


//---Liczby pierwsze--- to liczby naturalne więkrze od 1, które dzielą się tylko przez 1 i samą siebie:
// 2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59, ...
// Uwaga. Wartość int'a może zostać przekroczone  ( więc trzeba by int'a zwiękrzyć na inny typ by dzialalo,dla conajmniej 1000 liczb czyli do przedzialu 0 do 7919 int starcza  )
// Uwaga. BARDZO wolne obliczenia dla dużych liczb. Dla 1000 liczb tylko 2 sekundy. Dla przedzialu od 0 do 21474836 pierwsze przejscie dojscie do 1000 w przedziale zajmuje okolo 1 MINUTE CZASU.
// Wiecej na matematyka.pisz.pl    		  pierwsze 1000 liczb nas stronie:	 http://www.algorytm.edu.pl/algorytmy-maturalne/badanie-czy-liczba-pierwsza/1000-liczb-pierwszych-1.html
// Liczby pierwsze: im większe wartości liczbowe tym rzadziej zaczynają się one pojawiać. Dodatkowo, im większa wartość liczby tym dłuższy czas weryfikacji wszystkich potencjalnych dzielników.


public class klasa_1 {

    public static void main(String[] args)
    {
      metoda2();

    }





    private static void metoda2()
    {

        int a = 0;
        int k=0;
        int dlugosc_przedzialu=7919;  //np,: 100. (przedzial od 0 do 7919 daje lacznie 1000 liczb),

        System.out.println("Liczby pierwsze w przedziale od 0 do " + dlugosc_przedzialu + " : " ); // moge powiekrzyc zbior


        for ( int i = 0; i <= dlugosc_przedzialu; i++) // wypisanie np. 1:1=1 i ta pierwsza cyfra do 100 się tu zmienia , bez 1 bo liczby naturalne wiekrze od 1, tutaj bylo 100 zamiast zmiennej,wczesniej bylo:( int i = 0; i <= 100; i++)
        {
            for (int j = 1; j <= dlugosc_przedzialu; j++)  // wypisanie np. 1:1=1 i ta --druga-- cyfra do 100 się tu zmienia, tutaj bylo 100 zamiast zmiennej,wczesniej bylo: ( int j=1; j<=100; j++)
            {

                a = i / j;


                if (i == a * j)                 // to chyba sprawdza czy liczba calkowita
                {
                    k++;
                }


                if (j == dlugosc_przedzialu)               // j==100 bylo. Zmienilem na zmienna : "dlugosc_przedzialu"
                {
                    if (k == 2)
                    {
                        System.out.print(i + " "); // "i" jest liczba pierwsza
                    }
                }


                if (j == dlugosc_przedzialu)             // zerowanie k po petli gdy konczy sie petla j, tu bylo 100 zmienilem na "dlugosc_przedzialu"
                {
                    k = 0;
                }

            }
        }
    }
}




