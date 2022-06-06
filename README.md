# Metot-Tan-mlama
karenın alanını hesaplayan program

using System;

using System.Collections.Generic;

using System.Linq;

using System.Text;

using System.Threading.Tasks;


namespace fonksiyonlar_p

{

    internal class Program

    {
        public static void Main(string[] args) 

        {
            int kenar, alan;

            Console.WriteLine("Kenar Uzunluğunu Giriniz : ");

            kenar = Convert.ToInt32(Console.ReadLine());

            alan = carp(kenar);
            Console.WriteLine(alan);

            Metotlar ornek = new Metotlar();
            ornek.Yazdirekran(Convert.ToString(alan));  
            
            
            /*istenilen kısımlar açıklama kısmına dönüştürülüp farklı sonuçlar elde edilebilir. Şu an da değeri artmış şekilde karenin alanını yazdıracaktır.
            örnek hepsini çalıştırıyor.*/ 

            alan= ornek.arttırvetopla(ref kenar);

            ornek.Yazdirekran(Convert.ToString(alan));

            ornek.Yazdirekran(Convert.ToString(kenar * kenar));


            alan = kenar * kenar;

            Console.WriteLine("Karenin Alanı : " + alan);

            Console.ReadKey();
        }

        public static int carp(int deger1)
        {
            return (deger1 * deger1);
        }

        

    }
    class Metotlar
    {
        public void Yazdirekran(string veri)
        {
            Console.WriteLine(veri);
        }

        public int arttırvetopla(ref int deger1 )
        {
            deger1 += 1;
            return deger1;
        }
    }
    
}

[Patika Dev Sayfam](https://app.patika.dev/sevaalnuur)