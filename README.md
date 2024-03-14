import java.util.Scanner;

public class KDVTutariHesaplama {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Lütfen para miktarını girin:");
        double paraMiktari = scanner.nextDouble();

        double kdvOrani;
        if (paraMiktari > 0 && paraMiktari <= 1000) {
            kdvOrani = 0.18;
        } else {
            kdvOrani = 0.08;
        }

        double kdvTutari = paraMiktari * kdvOrani;
        double kdvliFiyat = paraMiktari + kdvTutari;

        System.out.println("Girilen para miktarı: " + paraMiktari + " TL");
        System.out.println("KDV Oranı: %" + (kdvOrani * 100));
        System.out.println("KDV Tutarı: " + kdvTutari + " TL");
        System.out.println("KDV'li Fiyat: " + kdvliFiyat + " TL");
    }
}
