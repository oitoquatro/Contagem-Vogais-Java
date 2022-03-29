import java.util.Scanner;

//Criar um programa que mostre um relatório de quantidades de vogais que aparecem em uma sequência:
//Para isso deverá:
//    a) Criar uma sub-rotina chamada gerarSequencia(), que:
//        ◦ receba, como parâmetro, a quantidade de elementos da sequência;
//        ◦ crie um vetor de caracteres com base na quantidade recebida pelo parâmetro;
//        ◦ preencha o vetor utilizando a entrada padrão (Scanner);
//        ◦ e retorne este vetor preenchido.
//    b) Criar uma sub-rotina chamada imprimirRelatorio(), que:
//        ◦ receba, como parâmetro, o vetor de vogais;
//        ◦ analise a quantidade de cada vogal existente no vetor;
//        ◦ e imprima a quantidade de cada vogal.
//    c) O programa principal deverá solicitar a entrada do tamanho da sequência de vogais,
//             e, logo após, deverá utilizar as sub-rotinas criadas acima.

public class exercicios06 {

	public static void main(String[] args) {
		Scanner leitor = new Scanner(System.in);
		
		System.out.print("Digite a quantidade de elementos do vetor: ");
		int n = leitor.nextInt();
		
		char sequencia[] = gerarSequencia(n);
		
		imprimirRelatorio(sequencia);
		
		leitor.close();		

	}
	
	public static char[] gerarSequencia(int n) {
		
		Scanner leitor = new Scanner(System.in);
		
		char v[] = new char[n];
		
	    for (int i = 0; i < v.length; i ++) {
	    	System.out.printf("v[%d] = ", i);
	    	v[i] = leitor.next().charAt(0);
	    	
	    }
	    
	    leitor.close();
	    
	    return v;
		
	}
	
	public static void imprimirRelatorio(char[] v) {
		
		int contA = 0, contE = 0, contI = 0, contO = 0, contU = 0;
		
		for (int i = 0; i < v.length; i ++) {
			switch (v[i]) {
			case 'A':
			case 'a': contA++; break;
			
			case 'E':
			case 'e': contE++; break;
			
			case 'I':
			case 'i': contI++; break;
			
			case 'O':
			case 'o': contO++; break;
			
			case 'U':
			case 'u': contU++; break;			
			
			}
		}
		
		System.out.println("Relatório de contagem de vogais");
		System.out.printf("Letra A: %d\n", contA);
		System.out.printf("Letra E: %d\n", contE);
		System.out.printf("Letra I: %d\n", contI);
		System.out.printf("Letra O: %d\n", contO);
		System.out.printf("Letra U: %d\n", contU);
	}

}
