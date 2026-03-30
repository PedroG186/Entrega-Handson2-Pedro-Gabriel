# Entrega-Handson2-Pedro-Gabriel

//atividade 1---------------------------------------------------------------------------------------------------

import java.util.Scanner;

public class trabalhoHandsOn {
    public static void main(String[] args) {
        System.out.println(" +'''''+");
     System.out.println(   "[| o o |]" );
        System.out.println(" |  ^  |");
        System.out.println(" | '-' |"); 
        System.out.println(" +-----+");

//Atividade 2-----------------------------------------------------------------------------------------------------------

import java.util.Scanner;


public class trabalhohandson2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        double lat1 = 25.0; 
        double lon1 = 35.0;
        double lat2 = 35.5;
        double lon2 = 25.5;

        double raioTerra = 6371.01;

        double x1 = Math.toRadians(lat1);
        double y1 = Math.toRadians(lon1);
        double x2 = Math.toRadians(lat2);
        double y2 = Math.toRadians(lon2);

        double distancia = raioTerra * Math.acos(Math.sin(x1) * Math.sin(x2) + Math.cos(x1) * Math.cos(x2) * Math.cos(y1 - y2));

        System.out.println("A distância entre os pontos é: " + distancia + " km");




    }
}



//Atividade3------------------------------------------------------------------------------------------------------------------------------

import java.util.Scanner;
public class trabalhohandson3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Digitem uma palavra ou frase: ");
        String texto = sc.nextLine();

        int  letras =0, numeros = 0, simbolos = 0, espacos = 0;

        for (char c : texto.toCharArray()) {
            if (Character.isLetter(c)) {
                letras++;
            } else if (Character.isDigit(c)) {
                numeros++;
            } else if (Character.isWhitespace(c)) {
                espacos++;
            } else {
                simbolos++;
            }
        }
        System.out.println("Letras: " + letras);
        System.out.println("Números: " + numeros);
        System.out.println("Símbolos: " + simbolos);
        System.out.println("Espaços: " + espacos);
    }
}


//Atividade 4------------------------------------------------------------------------------------------------------------------------

import java.util.Scanner;

public class trabalhohandson4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String resposta;
        int tentativas = 0;
        boolean acertou = false;

        System.out.println(" Quiz de Estrutura de Dados ");
        
    
        do {
            tentativas++;
            System.out.println("\nQuestão " + tentativas + "/3:");
            System.out.println("Qual estrutura de dados utiliza o princípio FIFO (First In, First Out)?");
            System.out.println("a) Pilha (Stack)");
            System.out.println("b) Fila (Queue)");
            System.out.println("c) Lista Ligada");
            System.out.println("d) Árvore Binária");
            System.out.println("e) Hash Table");
            System.out.print("Escolha a opção correta (a-e): ");
            
            resposta = scanner.next().toLowerCase(); 

            
            switch (resposta) {
                case "b":
                    System.out.println("Resposta correta! Você acertou na tentativa " + tentativas + ".");
                    acertou = true;
                    break;
                case "a":
                case "c":
                case "d":
                case "e":
                    System.out.println("Resposta incorreta.");
                    break;
                default:
                    System.out.println("Opção inválida. Tente novamente.");
                    break;
            }

            if (acertou) break; 

        } while (tentativas < 3);

        if (!acertou) {
            System.out.println("\nResposta incorreta nas 3 tentativas.");
        }

        scanner.close();
    }
}
----------------------------------------------------------------------------------------------------------------------------------------













































