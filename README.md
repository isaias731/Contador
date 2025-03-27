package System.out;

import java.util.Scanner;

public class Contador {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Digite o número inicial: ");
            int inicio = scanner.nextInt();

            System.out.print("Digite o número final: ");
            int fim = scanner.nextInt();

            if (inicio > fim) {
                System.out.println("O número inicial deve ser menor ou igual ao número final.");
                return;
            }

            System.out.println("Contagem de " + inicio + " até " + fim + ":");
            for (int numero = inicio; numero <= fim; numero++) {
                System.out.println(numero);
            }

        } catch (java.util.InputMismatchException e) {
            System.out.println("Entrada inválida. Por favor, digite números inteiros.");
        } finally {
            scanner.close();
        }
    }
}
