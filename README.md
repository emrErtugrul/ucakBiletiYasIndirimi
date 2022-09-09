# ucakBiletiYasIndirimi


import java.util.Scanner;

public class Main {

    public static void main(String[] args) 
    
        Scanner inp = new Scanner(System.in);
        double km;
        double age, normalTutar, yasIndirim, indirimliTutar, ggTutar, toplamTutar;
        double ytip;
        System.out.println("Mesafeyi km türünden giriniz : ");
        km = inp.nextDouble();
        System.out.println("Yaşınızı giriniz : ");
        age = inp.nextDouble();

        if (km < 0 || age < 0) {
            System.out.println("Hatalı Veri Girdiniz !");
        }

        System.out.println("Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ):");
        ytip = inp.nextDouble();
        if (ytip >= 1 || ytip <= 2) {
        } else {
            System.out.println("Hatalı Veri Girdiniz !");
        }

        normalTutar = km * 0.10;
        if (ytip == 2) {
            if (age < 12) {
                yasIndirim = normalTutar * 0.50;
                indirimliTutar = normalTutar - yasIndirim;
                ggTutar = indirimliTutar * 0.20;
                toplamTutar = (indirimliTutar - ggTutar) * 2;
                System.out.println(toplamTutar + " Tl");

            } else if (age <= 12 || age <= 24) {
                yasIndirim = normalTutar * 0.10;
                indirimliTutar = normalTutar - yasIndirim;
                ggTutar = indirimliTutar * 0.20;
                toplamTutar = (indirimliTutar - ggTutar) * 2;
                System.out.println(toplamTutar + " Tl");

            } else if (age > 65) {
                yasIndirim = normalTutar * 0.30;
                indirimliTutar = normalTutar - yasIndirim;
                ggTutar = indirimliTutar * 0.20;
                toplamTutar = (indirimliTutar - ggTutar) * 2;
                System.out.println(toplamTutar + " Tl");

            }else if (age > 24 && age < 66) {

                indirimliTutar = normalTutar ;
                toplamTutar = (indirimliTutar*2) ;
                System.out.println(toplamTutar + " Tl");
            }
        } else if (ytip == 1) {
            System.out.println(ytip);
            if (age < 12) {
                yasIndirim = normalTutar * 0.50;
                indirimliTutar = normalTutar - yasIndirim;
                toplamTutar = (indirimliTutar) * 2;
                System.out.println(toplamTutar + " Tl");

            } else if (age <= 12 || age <= 24) {
                yasIndirim = normalTutar * 0.10;
                indirimliTutar = normalTutar - yasIndirim;
                toplamTutar = (indirimliTutar) * 2;
                System.out.println(toplamTutar + " Tl");

            } else if (age > 65) {
                yasIndirim = normalTutar * 0.30;
                indirimliTutar = normalTutar - yasIndirim;
                toplamTutar = (indirimliTutar) * 2;
                System.out.println(toplamTutar + " Tl");

            } else if (age > 24 && age < 66) {

                indirimliTutar = normalTutar ;
                toplamTutar = (indirimliTutar) ;
                System.out.println(toplamTutar + " Tl");
            }
        }
    }
}
