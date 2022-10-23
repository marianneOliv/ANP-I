# ANP-I
Atividade ANP I- POO

public class festa {
    public static void main(String[] args) {
        ArrayList<Visitante> Visitantes = new ArrayList<>();
        
        int options, isRunning = 1;
        
        ArrayList<String> cidades = new ArrayList<String>();
        int quantHomens = 0, quantMulheres = 0, quantMenores = 0;
        
        while(isRunning == 1) {
            options = Integer.parseInt(JOptionPane.showInputDialog("1) Novo cadastro \n2) Mostrar resultado \n3) Fechar"));
            
            if (options == 1) {
                Visitante v = new Visitante();
                
                v.setNome(JOptionPane.showInputDialog("Informe o nome:"));
                v.setCidadeResidencia(JOptionPane.showInputDialog("Informe a cidade:"));
                v.setSexo(JOptionPane.showInputDialog("Informe o sexo (F ou M):"));
                v.setProfissao(JOptionPane.showInputDialog("Informe a profissão"));
                v.setFone (JOptionPane.showInputDialog("Telefone:"));
                v.setNascimento(Integer.parseInt(JOptionPane.showInputDialog("Ano de nascimento (AAAA):")));
                
                if (v.getNascimento() > 2004 ) {
                    quantMenores++;
                }
                
                if (v.getSexo().equals("M")) {
                    quantHomens++;
                } else if (v.getSexo().equals("F")) {
                    quantMulheres++;
                }
                
                if (!cidades.contains(v.getCidadeResidencia())) {
                    cidades.add(v.getCidadeResidencia());
                }
                
                Visitantes.add(v);
            } else if (options == 2) {
                JOptionPane.showMessageDialog(null, "INFO\n\n Total: "+ Visitantes.size() + "\n Homens: " + quantHomens + " - " + (quantHomens * 100 / Visitantes.size()) + "%" + "\n Mulheres: " + quantMulheres + " - " + (quantMulheres * 100 / Visitantes.size()) + "%" + "\n Menores de Idade: " + quantMenores + "\n Cidades: " + cidades.size());
            } else {
                isRunning = 0;
            }
            
        }
    }
}
