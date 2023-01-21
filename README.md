import java.util.Scanner;

public class mainOf {
	public static void main(String[] args) {
		int diaNasc;
		int mesNasc = 0;
		int anoNasc;
		float altura;
		float peso;
		String nome;
		String sexo;
		String signo;
		String titulo;
		String resultIMC;
		float imc;
		Scanner leia = new Scanner(System.in);

	System.out.println("nome completo");
	nome=leia.nextLine();
	
		
	System.out.println("dia que nasceu");
	diaNasc=leia.nextInt();
	while (diaNasc < 0 || diaNasc > 31) {
		System.out.println("ERROOU, dia inválido");
		System.out.println("dia que nasceu");
		diaNasc=leia.nextInt();
	}
	
	System.out.println("mês que nasceu");
	mesNasc=leia.nextInt();
	while (mesNasc < 0 || mesNasc > 12) {
		System.out.println("ERROOU, m inválido");
		System.out.println("mês que nasceu");
		mesNasc=leia.nextInt();
	}
	
	System.out.println("ano que nasceu");
	anoNasc=leia.nextInt();
	
	System.out.println("Qual seu sexo");
	sexo=leia.next();
	
	System.out.println("Qual a sua altura");
	altura=leia.nextFloat();
	
	System.out.println("Qual o seu peso");
	peso=leia.nextFloat();
	
	imc = peso / (altura *  altura);
	
	if (imc < 18.5) {
		resultIMC = " está só o pó, precisa treinar mais";
	}
	else {
		if(imc > 24.9) {
			resultIMC = " está fofis, precisa treinar mais";
		}
		else {
			if(sexo.equalsIgnoreCase("m")) {
				resultIMC = " está top, pronto para guerrear";
			}
			else {
				resultIMC = " está top, pronta para guerrear";				
			}
		}
	}
	
	if (sexo.equalsIgnoreCase("F")) {
		titulo = "Amazona";
	} else {
		titulo = "Cavaleiro";
	}
	
	if (mesNasc == 1) {
		if (diaNasc < 21) {
			signo = "Capricornio";
		}
		else {
			signo = "Aquario";
		}	
	}
	else {
		if(mesNasc == 2) {
			if(diaNasc < 20) {
				signo = "Aquario";
			}
			else {
				signo = "Peixes";
			}
		}
		else {
			if(mesNasc==3) {
				if(diaNasc < 21) {
					signo = "Peixes";
				}
				else {
					signo = "Aries";
				}
			}
			else {
				if(mesNasc==4) {
					if(diaNasc < 21) {
						signo = "Aries";
					}
					else {
						signo = "Touro";
					}
				}
				else {
					if(mesNasc==5) {
						if(diaNasc < 21) {
							signo = "Toura";
						}
						else {
							signo ="Gêmeos";
						}
					}
					if(mesNasc==6) {
						if(diaNasc < 21) {
							signo = "Gêmeos";
						}
						else {
							signo ="Câncer";
						}
					}
					else {
						if(mesNasc==7) {
							if(diaNasc < 23) {
								signo = "Câncer";
							}
							else {
								signo = "Leão";
							}
						}
						if(mesNasc==8) {
							if(diaNasc < 23) {
								signo = "Leão";
							}
							else {
								signo = "Virgem";
							}
						}
						else {
							if(mesNasc==9) {
								if(diaNasc<23) {
									signo="Virgem";
								}
								else {
									signo="Libra";
								}
							}
							else {
								if(mesNasc==10) {
									if(diaNasc<23) {
										signo="Libra";
									}
									else {
										signo="Escorpião";
									}
								}
								else {
									if(mesNasc==11) {
										if(diaNasc<22) {
											signo="Escorpião";
										}
										else {
											signo="Sargitário";
										}
									}
									else {
										if(diaNasc<22) {
											signo="Sargitário";
										}
										else {
											signo="Capricornio";
										}
									}
								}
								
							}
						}
					}
				}
			}
		}
	}
	
	System.out.println(nome + ", " + titulo +
			" de " + signo + ".");
	System.out.println(titulo + resultIMC);
	
	leia.close();
	
	}
}
