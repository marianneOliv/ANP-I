# ANP-I
Atividade ANP I- POO

package elevador;

import java.util.Scanner;
import javax.swing.JOptionPane;

/**
 *
 * @author OMARI
 */
public class ExecutaElevador {
    public static void main(String[] args) {
        Scanner ler= new Scanner (System.in);
        int aux;
        
        Elevador e1 = new Elevador() ;
        e1.inicializa();
        e1.setAndarAtual(10);
        e1.setQuantidade(5);
        e1.Entra();
        e1.desce();
        
         System.out.println("Elevador 1:\n" + e1.toString());
         
        Elevador e2= new Elevador();
        e2.inicializa();
        e2.desce();
        e2.sobe();
        e2.Entra();
        e2.sobe();
        e2.Entra();
        System.out.println("Elevador 2:\n"+e2.toString());
    }
}
