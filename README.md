# reajusteSalJv

import java.util.Scanner;

public class ReajusteSalarial {

   import java.util.Scanner;

public class ReajusteSalarial {

    public static void main(String[] args) {
       
        Scanner scanner = new Scanner(System.in);
        
        
        System.out.print("Digite o salário atual do colaborador: R$");
        double salarioAtual = scanner.nextDouble();
        
     
        scanner.close();
        
   
        double aumentoPer = 0;
        double aumentoVal = 0;
        double novoSal = 0;
        double aumentoReal = 0;
        double infla = 3.8;

        
        if (salarioAtual <= 280.00) {
            aumentoPer= 20;
        } else if (salarioAtual <= 700.00) {
            aumentoPer = 15;
        } else if (salarioAtual <= 1500.00) {
            aumentoPer= 10;
        } else {
            aumentoPer = 5;
        }

        aumentoVal = salarioAtual * aumentoPer / 100;
        
      
        novoSal = salarioAtual + aumentoVal;
        
      
        aumentoReal = aumentoVal * (1 - infla / 100);
        
        System.out.println("\nResultados:");
        System.out.printf("Salário antes do reajuste: R$%.2f\n", salarioAtual);
        System.out.printf("Percentual de aumento aplicado: %.0f%%\n", aumentoPer);
        System.out.printf("Valor do aumento: R$%.2f\n", aumentoVal);
        System.out.printf("Novo salário após o aumento: R$%.2f\n", novoSala);
        System.out.printf("Valor do aumento real, descontado a inflação: R$%.2f\n", aumentoReal);
    }
}
