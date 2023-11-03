# konversi
package PemrogramanDasar.Aok;
import java.util.Scanner;
public class KonversiBilangan {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Pilih bilangan : \n1. Desimal\n2. Biner\n3. Heksadesimal");
        System.out.print("Pilih menu tersebut (1/2/3): ");
        int pilihan = input.nextInt();
        System.out.println("Menu yang dipilih : "+pilihan);
        
        switch (pilihan){
            case 1:
                System.out.println("Menu : \n1. Desimal ke biner\n2. Desimal ke heksadesimal");
                System.out.print("Pilihan menu (1/2): ");
                int pilih = input.nextInt();
                System.out.println("Menu yang dipilih : "+pilih);
                
                if (pilih== 1){
                    System.out.print("Masukan bilangan desimal : ");
                    int angka = input.nextInt();
                    String binerd;
                    binerd = Integer.toBinaryString(angka);
                    System.out.println("Bilangan binernya adalah = "+binerd+" "); 
                }
                if (pilihan == 2){
                    System.out.print("Masukan bilangan desimal : ");
                    int angka = input.nextInt();
                    String heksad;
                    heksad = Integer.toHexString(angka);
                    System.out.println("Bilangan heksadesimalnya adalah : "+heksad);
                } 
                break;
                
            case 2:
                System.out.println("Menu : \n1. Biner ke desimal\n2. Biner ke heksadesimal");
                System.out.print("Pilih menu tersebut (1/2): ");
                int pilihb = input.nextInt();
                System.out.println("Menu yang dipilih : "+pilihb);
                
                if (pilihb== 1){ 
                    System.out.print("Masukan bilangan biner : ");
                    String angkab = input.next();
                    int desimal = Integer.parseInt(angkab,2);
                    System.out.println("Bilangan desimalnya adalah = "+desimal);
                }
                if (pilihb == 2){
                    System.out.print("Masukan bilangan biner : ");
                    int angka2 = input.nextInt();
                    String heksab = Integer.toHexString(angka2);
                    System.out.println("Bilangan heksadesimalnya adalah = "+heksab);
                }
                break;
                
            case 3:    
                System.out.println("Pilih : \n1. Heksadesimal ke desimal\n2. Heksadesimal ke biner");
                System.out.print("Pilih menu tersebut (1/2): ");
                int pilihc = input.nextInt();
                System.out.println("Menu yang dipilih : "+pilihc);
                
                if (pilihc == 1){
                    System.out.print("Masukan bilangan heksadesimal : ");
                    String angkah = input.next();
                    int desimalc = Integer.parseInt(angkah,16);
                    System.out.println("Bilangan desimal adalah = "+desimalc+" ");
                }
                if (pilihc == 2){
                    System.out.print("Masukan bilangan heksadesimal : ");
                    String angkac = input.next();
                    long heksa2 = Long.parseLong(angkac,16);
                    String binerh = Long.toBinaryString(heksa2);
                    System.out.println("Bilangan binernya adalah = "+binerh); 
                }
                break;
        }   
    }
    
}
