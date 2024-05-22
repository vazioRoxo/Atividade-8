import java.util.ArrayList;
import java.util.Scanner;

public class Principal {
    private static ArrayList<Empregado> empregados = new ArrayList<>();
    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int opcao;
        do {
            System.out.println("Menu:");
            System.out.println("1. Criar novo empregado");
            System.out.println("2. Promover empregado");
            System.out.println("3. Aumentar salário do empregado");
            System.out.println("4. Demitir empregado");
            System.out.println("5. Fazer aniversário do empregado");
            System.out.println("6. Mostrar detalhes dos empregados");
            System.out.println("7. Sair");
            System.out.print("Escolha uma opção: ");
            opcao = scanner.nextInt();
            scanner.nextLine(); 

            switch (opcao) {
                case 1:
                    criarEmpregado();
                    break;
                case 2:
                    promoverEmpregado();
                    break;
                case 3:
                    aumentarSalarioEmpregado();
                    break;
                case 4:
                    demitirEmpregado();
                    break;
                case 5:
                    fazerAniversarioEmpregado();
                    break;
                case 6:
                    mostrarEmpregados();
                    break;
                case 7:
                    System.out.println("Saindo...");
                    break;
                default:
                    System.out.println("Opção inválida.");
            }
        } while (opcao != 7);
    }

    private static void criarEmpregado() {
        System.out.print("Digite o nome do empregado: ");
        String nome = scanner.nextLine();
        System.out.print("Digite a idade do empregado: ");
        int idade = scanner.nextInt();
        System.out.print("Digite o salário do empregado: ");
        double salario = scanner.nextDouble();
        scanner.nextLine(); 

        empregados.add(new Empregado(nome, idade, salario));
        System.out.println("Empregado criado com sucesso.");
    }

    private static void promoverEmpregado() {
        Empregado empregado = selecionarEmpregado();
        if (empregado != null) {
            empregado.promover();
        }
    }

    private static void aumentarSalarioEmpregado() {
        Empregado empregado = selecionarEmpregado();
        if (empregado != null) {
            System.out.print("Digite o percentual de aumento: ");
            double percentual = scanner.nextDouble();
            scanner.nextLine(); 
            empregado.aumentarSalario(percentual);
            System.out.println("Salário aumentado com sucesso.");
        }
    }

    private static void demitirEmpregado() {
        Empregado empregado = selecionarEmpregado();
        if (empregado != null) {
            System.out.println("Motivos de demissão:");
            System.out.println("1. Justa causa");
            System.out.println("2. Decisão do empregador");
            System.out.println("3. Aposentadoria");
            System.out.print("Digite o motivo da demissão: ");
            int motivo = scanner.nextInt();
            scanner.nextLine(); 
            empregado.demitir(motivo);
        }
    }

    private static void fazerAniversarioEmpregado() {
        Empregado empregado = selecionarEmpregado();
        if (empregado != null) {
            empregado.fazerAniversario();
            System.out.println("Feliz aniversário! Idade atualizada.");
        }
    }

    private static void mostrarEmpregados() {
        if (empregados.isEmpty()) {
            System.out.println("Nenhum empregado cadastrado.");
        } else {
            for (Empregado empregado : empregados) {
                System.out.println(empregado);
            }
        }
    }

    private static Empregado selecionarEmpregado() {
        if (empregados.isEmpty()) {
            System.out.println("Nenhum empregado cadastrado.");
            return null;
        }
        mostrarEmpregados();
        System.out.print("Digite o número do empregado: ");
        int index = scanner.nextInt() - 1;
        scanner.nextLine();
        if (index >= 0 && index < empregados.size()) {
            return empregados.get(index);
        } else {
            System.out.println("Empregado inválido.");
            return null;
        }
    }
}
