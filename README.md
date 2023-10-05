# VEICULOMOTO

package Automovel;

public class Moto implements Veiculo{

	private String marca;
	private String modelo;
	private int velocidade;
	private int marcha;
	private boolean ligado; 
	
	@Override
	public void ligar() {
		if(this.ligado==false && this.velocidade==0)
			this.ligado = true;
		else
			System.out.println("Erro ao ligar a moto");
		
	}

	@Override
	public void desligar() {
		if(this.ligado==true && this.velocidade==0)
			this.ligado = false;
		else
			System.out.println("Erro ao desligar a moto");
		
	}

	@Override
	public void acelerar() {
		if(this.ligado ==true && this.marcha>0)
			this.velocidade+=3;
		System.out.println("Problema na aceleração");
		
	}

	@Override
	public void freiar() {
		if(this.ligado==true && this.velocidade>0)
			this.velocidade-=3;
		else
			System.out.println("Problemas na frenagem");
	}

	@Override
	public void trocarMarcha() {
		if(this.ligado==true && this.velocidade>0)
			this.marcha++;
		
	}

	public String getMarca() {
		return marca;
	}

	public void setMarca(String marca) {
		this.marca = marca;
	}

	public String getModelo() {
		return modelo;
	}

	public void setModelo(String modelo) {
		this.modelo = modelo;
	}

	public int getVelocidade() {
		return velocidade;
	}

	public int getMarcha() {
		return marcha;
	}

	public boolean getLigado() {
		return ligado;
	}	
	}
	
