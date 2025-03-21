class Pessoa {
  double _altura = 0, _peso = 0;

  // Getters e Setters compactos
  double get altura => _altura;
  set altura(double novaAltura) => _altura = novaAltura;

  double get peso => _peso;
  set peso(double novoPeso) => _peso = novoPeso;

  // Cálculo do IMC
  double get imc => _peso / (_altura * _altura);

  // Classificação do IMC
  String get classificacao => 
    imc < 18.5 ? "Abaixo do peso" :
    imc < 24.9 ? "Peso normal" :
    imc < 29.9 ? "Sobrepeso" : "Obesidade";
}

void main() {
  var pessoa = Pessoa();
  
  // Usando os setters para definir os valores
  pessoa.altura = 1.80;
  pessoa.peso = 80;

  print("Você pesa ${pessoa.peso.toStringAsFixed(2)} Kg");
  print("Você mede ${pessoa.altura.toStringAsFixed(2)} M");
  print("Seu IMC é ${pessoa.imc.toStringAsFixed(2)}");
  print("Classificação: ${pessoa.classificacao}");
}
