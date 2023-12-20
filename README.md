
import java.util.Scanner;

public class test {
    public static void main(String[] args) {
        int mesafe, yas, yolculukTipi;
        Scanner input = new Scanner(System.in);
        double normalTutar, yasİndirimi, İndirimliTutar, gidisDonusBiletIndirimi, toplamTutar;
        System.out.println("Mesafe (KM) Giriniz:");
        mesafe = input.nextInt();

        System.out.println("Yaşınızı giriniz.");
        yas = input.nextInt();

        System.out.println("Yolculuk tipini giriniz( 1 => Tek yön , 2=> Gidiş-Dönüş)");
        yolculukTipi = input.nextInt();
        normalTutar = mesafe * 0.10;

        if (yas < 12) {
            yasİndirimi = normalTutar * 0.50;
            İndirimliTutar = normalTutar - yasİndirimi;
            System.out.println("İndirimli toplam tutar:" + İndirimliTutar);
        }
        if (yas > 12 && yas <= 24) {
            yasİndirimi = normalTutar * 0.10;
            İndirimliTutar = normalTutar - yasİndirimi;
            System.out.println("İndirimli toplam tutar:" + İndirimliTutar);
        }
        if (yas > 65) {
            yasİndirimi = normalTutar * 0.30;
            İndirimliTutar = normalTutar - yasİndirimi;
            System.out.println("İndirimli toplam tutar:" + İndirimliTutar);
        }
        if(yas >= 0 && yolculukTipi==2)
        {
            gidisDonusBiletIndirimi = normalTutar * 0.20;
            System.out.println("İndirimli toplam tutar:" + gidisDonusBiletIndirimi);

        }
        else
        {
            System.out.println("Hatalı Veri Girdiniz !");
        }





    }
}



