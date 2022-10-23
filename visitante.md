# ANP-I
Atividade ANP I- POO

public class Visitante {
    private String nome;
    private String fone;
    private String cidadeResidencia;
    private String sexo;
    private String profissao;
    private int nascimento;
    
        
    public String getNome() {
        return nome;
    }
        
    public String getFone() {
        return fone;
    }

    public String getCidadeResidencia() {
        return cidadeResidencia;
    }

    public String getSexo() {
        return sexo;
    }

    public String getProfissao() {
        return profissao;
    }

    public int getNascimento() {
        return nascimento;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public void setFone(String fone) {
        this.fone = fone;
    }

    public void setCidadeResidencia(String cidadeResidencia) {
        this.cidadeResidencia = cidadeResidencia;
    }

    public void setSexo(String sexo) {
        this.sexo = sexo;
    }

    public void setProfissao(String profissao) {
        this.profissao = profissao;
    }

    public void setNascimento(int nascimento) {
        this.nascimento = nascimento;
    }
    
}
