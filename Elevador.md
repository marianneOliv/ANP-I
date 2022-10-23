# ANP-I
Atividade ANP I- POO

public class Elevador {

    private int andarAtual, total, capacidade,quantidade;

    public Elevador() {
    }
 
    public Elevador(int andarAtual, int total, int capacidade, 
            int quantidade) {
        this.andarAtual = andarAtual;
        this.total = 15;
        this.capacidade =8;
        this.quantidade = quantidade;
    }

    @Override
    public String toString() {
        return "Andar Atual: " + andarAtual + " Total de Andares: " + total + ","
        + " Capacidade Maxima: " + capacidade + ", Quantidade Atual: " + quantidade;    
    }

    public void setQuantidade(int quantidade) {
        this.quantidade = quantidade;
    }

    public void setAndarAtual(int andarAtual) {
        this.andarAtual = andarAtual;
    }

    public int getAndarAtual(int andarAtual) {
        return this.andarAtual;
    }

    public int getQuantidade() {
        return this.quantidade;
    }
    
    public void inicializa(){
        this.quantidade=0;
        this.andarAtual=0; 
        this.total=15;
        this.capacidade=8;
    }

    public void sobe () {
        if (this.andarAtual>=andarAtual && andarAtual<this.total) {
            this.andarAtual= andarAtual+=1;
    }
     else{
            System.out.println("Ultimo andar: "+ andarAtual);      
    }
    }
    public void desce(){
        if (andarAtual <= this.total && andarAtual>=1) {
            this.andarAtual =andarAtual-=1;
        }
        else {
            System.out.println("Terreo");;
    }       
    }    

    public int Entra() {
           if (quantidade > this.capacidade) {
               System.out.println("Capacidade maxima excedida"); 
               return quantidade;
    }
            else {
               return quantidade+=1;
    }
    }
    public void sai() {
            if (this.quantidade>0) {
            this.quantidade= quantidade-=1;
    }
            else{
                System.out.println("Elevador vazio");
    }
    }     
   
