# Codi d'exemple:

Us adjunto exemple de codi per al programa de banc d'aliments:

```
import java.util.Scanner;

public class principal {

    private static Scanner sc = new Scanner(System.in);
    private static String[] arrayNomAliments = new String[100];
    private static int[] arrayQuantitatAliments = new int[100];

    public static void llistarAliments() {

        System.out.println("Llista de aliments:");
        for (int i = 0; i < arrayNomAliments.length; i++) {
            if (arrayNomAliments[i] != null) {
                System.out.println(arrayNomAliments[i]);
            }
        }
    }

    public static void altaAliment() {
        System.out.println("Introdueixi nom del aliment: ");
        String opcio = sc.nextLine();

        for (int i = 0; i < arrayNomAliments.length; i++) {
            if (arrayNomAliments[i] == null) {
                arrayNomAliments[i] = opcio;
                arrayQuantitatAliments[i] = 0;
                break;
            }
        }

    }

    public static void modificarAliment() {
        llistarAliments();
        System.out.println("Quin aliment vol modificar? ");
        String opcio = sc.nextLine();
        System.out.println("Quin es el nou nom? ");
        String nomNou = sc.nextLine();

        for (int i = 0; i < arrayNomAliments.length; i++) {
            if (arrayNomAliments[i] != null) {
                if (arrayNomAliments[i].equals(opcio)) {
                    arrayNomAliments[i] = nomNou;
                    break;
                }
            }
        }
    }

    public static void eliminarAliment() {
        llistarAliments();
        System.out.println("Quin aliment vol eliminar? ");
        String opcio = sc.nextLine();

        for (int i = 0; i < arrayNomAliments.length; i++) {
            if (arrayNomAliments[i] != null) {
                if (arrayNomAliments[i].equals(opcio)) {
                    arrayNomAliments[i] = null;
                    break;
                }
            }
        }
        System.out.println("No s'ha trobat el nom de aliment a eliminar.");
    }

    public static boolean menuAliments() {
        boolean sortir = false;

        System.out.println("**************************");
        System.out.println("Menu Aliments, seleccioni:");
        System.out.println("**************************");
        System.out.println("1.- Llistar aliments. ");
        System.out.println("2.- Alta aliment. ");
        System.out.println("3.- Modificar aliment. ");
        System.out.println("4.- Eliminar aliment. ");
        System.out.println("0.- Sortir");

        String opcio = sc.nextLine();

        if (opcio.equals("0")) {
            sortir = true;
        }
        if (opcio.equals("1")) {
            llistarAliments();
        }
        if (opcio.equals("2")) {
            altaAliment();
        }
        if (opcio.equals("3")) {
            modificarAliment();
        }
        if (opcio.equals("4")) {
            eliminarAliment();
        }

        return sortir;
    }

    public static void modificaEstocAliments(String nom, int kilos) {
        for (int i = 0; i < arrayNomAliments.length; i++) {
            if (arrayNomAliments[i] != null) {
                if (arrayNomAliments[i].equals(nom)) {
                    arrayQuantitatAliments[i] += kilos;
                    System.out.println("Els kilos de " + nom + " han incrementat en " + kilos);
                    break;
                }
            }
        }
        System.out.println("No s ha trobat el aliment.");
    }


    public static void donarAliments() {
        llistarAliments();

        System.out.println(" Quin aliment vol donar? ");
        String aliment = sc.nextLine();

        System.out.println(" Quants kg vol donar?");
        String kilos = sc.nextLine();
        try {
            modificaEstocAliments(aliment, Integer.parseInt(kilos));
        }catch (NumberFormatException e){
            System.out.println("La quantitat introduida no es correcte.");
        }


    }

    public static boolean menu() {
        boolean sortir = false;
        System.out.println("**************");
        System.out.println("Menu principal");
        System.out.println("**************");
        System.out.println("Benvingut, seleccioni:");
        System.out.println("1.- Gestionar aliments. ");
        System.out.println("2.- Donar aliments. ");
        System.out.println("0.- Sortir");

        String opcio = sc.nextLine();
        if (opcio.equals("0")) {
            sortir = true;
        }
        if (opcio.equals("1")) {
            while (!menuAliments()) {
            }
        }

        if (opcio.equals("2")) {
            donarAliments();
        }

        return sortir;

    }

    public static void main(String[] args) {


            while (!menu()) {

            }

    }

}

```
