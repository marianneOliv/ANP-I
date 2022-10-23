# ANP-I
Atividade ANP I- POO

package executacampeonato;

import java.util.ArrayList;
import javax.swing.JOptionPane;


public class ExecutaCampeonato {
    
     
    public static void main(String[] args) {
      ArrayList<Equipes> Equipes = new ArrayList<>();

      Equipes PrimeiroLugar = new Equipes();
      Equipes SegundoLugar = new Equipes();
      Equipes TerceiroLugar = new Equipes();
       
      int opcao, sair=0, n =0;
	
    while(sair != 5){
        
        opcao = (Integer.parseInt(JOptionPane.showInputDialog("1 - Cadastrar equipe \n 2 - Equipe Vencedora \n 3 - Tres primeiros colocados \n 4 - Total de equipes inscritas \n 5 - Sair: ")));
		
        if(opcao == 1){
         n++;
         Equipes equipes = new Equipes();
     
	 equipes.setNome(JOptionPane.showInputDialog("Nome da equipe: "));
         equipes.setCidade(JOptionPane.showInputDialog("Cidade: "));
         equipes.setTecnico(JOptionPane.showInputDialog("Nome do Tecnico: "));
         equipes.setEmail(JOptionPane.showInputDialog("Email da Equipe: "));
         equipes.setQuant(Integer.parseInt(JOptionPane.showInputDialog("Quantidade de pontos: ")));
         equipes.setVitorias(Integer.parseInt(JOptionPane.showInputDialog("Número de vitórias: ")));
         equipes.setSaldo(Integer.parseInt(JOptionPane.showInputDialog("Saldo de sets vencidos: ")));
         equipes.setColocacao(Integer.parseInt(JOptionPane.showInputDialog("Colocação final: ")));
         
         if (equipes.getColocacao() == 1){
             PrimeiroLugar = equipes;
         }
          if (equipes.getColocacao() == 2){
            SegundoLugar = equipes;
         }
          if (equipes.getColocacao() == 3){
             TerceiroLugar = equipes;
         }
         Equipes.add(equipes);
         
        } else if (opcao == 2){
           JOptionPane.showMessageDialog( null, "Equipe Vendecora: " + PrimeiroLugar.getNome() + "\n Cidade: " + PrimeiroLugar.getCidade() + "\n Tecnico: " + PrimeiroLugar.getTecnico() + "\n E-mial da equipe: " 
                   + PrimeiroLugar.getEmail() + "\n Quantidade de pontos: " + PrimeiroLugar.getQuant()
                   + "\n Numero de vitorias: " + PrimeiroLugar.getVitorias()+ "\n Saldo de sets vencidos: " + PrimeiroLugar.getSaldo() + "\n Colocacao: " + PrimeiroLugar.getColocacao() );
         
        } else if (opcao == 3){
            JOptionPane.showMessageDialog( null, "Tres primeiras equipes colocadas: \n Nome: "+ PrimeiroLugar.getNome() + "\\n Cidade: " + PrimeiroLugar.getCidade()+
                    "\n Nome: "+ SegundoLugar.getNome() + "\\n Cidade: " + SegundoLugar.getCidade() +
                    "\n Nome: "+ TerceiroLugar.getNome() + "\\n Cidade: " + TerceiroLugar.getCidade());
        } else if (opcao == 4){
            JOptionPane.showMessageDialog( null, " Quantidade de equipes inscritas: " + n);
        }
        
        if (opcao == 5){
            System.out.println("Voce saiu");
            sair = 5;
             
        }
    		
	}
    }
    
}
