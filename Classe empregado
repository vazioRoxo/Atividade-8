public class Empregado {
    private String nome;
    private int idade;
    private double salario;

    public Empregado(String nome, int idade, double salario) {
        this.nome = nome;
        this.idade = idade;
        this.salario = salario;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }

    public double getSalario() {
        return salario;
    }

    public void setSalario(double salario) {
        this.salario = salario;
    }

    public void promover() {
        if (this.idade > 18) {
            aumentarSalario(0.25);
        } else {
            System.out.println("Promoção não é para menores.");
        }
    }

    public void aumentarSalario(double percentual) {
        this.salario += this.salario * (percentual / 100);
    }

    public void demitir(int razao) {
        switch (razao) {
            case 1: 
                System.out.println("Empregado deve cumprir aviso prévio.");
                break;
            case 2: 
                double multa = this.salario * 0.40;
                System.out.println("Empregado demitido. Multa de 40% do salário: " + multa);
                break;
            case 3: 
                double salarioAposentadoria;
                if (this.salario >= 1000 && this.salario < 2000) {
                    salarioAposentadoria = 1500;
                } else if (this.salario >= 2000 && this.salario < 3000) {
                    salarioAposentadoria = 2500;
                } else if (this.salario >= 3000 && this.salario < 4000) {
                    salarioAposentadoria = 3500;
                } else {
                    salarioAposentadoria = 4000;
                }
                System.out.println("Empregado aposentado. Salário de aposentadoria: " + salarioAposentadoria);
                break;
            default:
                System.out.println("Motivo de demissão inválido.");
        }
    }

    public void fazerAniversario() {
        this.idade += 1;
    }

    @Override
    public String toString() {
        return "Empregado [Nome=" + nome + ", Idade=" + idade + ", Salário=" + salario + "]";
    }
}
