# Java---programy-dzialajace

//---------- Co robi program? : Wypisuje tabliczkę mnożenia w pliku .txt (notatnik) max wypisuje 10*10=100 -----------


    import java.io.FileNotFoundException;
            import java.io.PrintWriter;

public class tabliczka_mnozenia_zapis_txt_2{
    public static void main(String[] args) throws FileNotFoundException {
        PrintWriter zapis = new PrintWriter("tabliczka_mnozenia_zapis_txt_2.txt");



        int k=0;
        for (int i=1; i<=10; i++)
        {
            for (int j = 1; j <= 10; j++)
            {
                zapis.print(i * j + "      ");
                k=k+1;
                if (k>9)
                {
                    zapis.println();
                    k=0;
                }


            }
        }


     //   zapis.println("Ala ma kota, a kot ma Alę"); // ( ta linijka jest nie potrzebna)
        zapis.close();



    }
}
