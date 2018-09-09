# Calculadora

Calculadora simples em Javascript

## Descrição do projeto

Esse projeto serve para fins de aprendizado da linguagem de programação Javascript. Neste projeto é desenvolvido uma calculadora simples que faz as funções básicas de aritmética.

### Recuperação de valores

No exemplo abaixo é realizado uma função para recuperar os valores dos elementos com o ID "operacao", "num1" e "num2".

```
			function calcular(){
				//recuperando valores
				var operacao = document.getElementById('operacao').value;
				var num1 = document.getElementById('num1').value;
				var num2 = document.getElementById('num2').value;Give examples
```

### Convertendo os valores recuperados em Float

Quando recuperamos os valores dos elementos, recebemos eles como strings. E para realizarmos os cálculos precisamos converte-los para INT ou FLOAT. Neste caso iremos converte-los para FLOAT.

```
			num1 = parseFloat(num1);
			num2 = parseFloat(num2);
```

### Validando inputs
E agora utilizaremos a condição IF para validar os inputs.

```
			if(num1 == '' || num1 == null){
				alert('Favor digitar um valor válido (num1)');
				return false;
			}	

			if(num2 == '' || num2 == null){
				alert('Favor digitar um valor válido (num2)');
				return false;
			}
```

### Variável do Resultado
Criamos uma variavel para o resultado do nosso calculo.
```
		var resultado = null;
```

E agora por fim faremos o uso de switch para alojarmos os métodos para cada função aritmética que estamos trabalhando. Neste caso, no input de ID "operacao" foi posto 4 valores: 1 - subtração, 2-adição, 3-multiplicação e 4-divisão.

```
				switch(operacao){
					case '1':
					var resultado = num1 - num2;
					break;

					case '2':
					var resultado = num1 + num2;
					break;

					case '3':
					var resultado = num1 * num2;
					break;

					case '4':
					var resultado = num1 / num2;
					break;

					default:
						alert('A opção selecionada é inválida');
						return false;
				}
```

### Imprimindo o resultado

No input com ID "resultado" iremos dizer que o seu valor é "resultado"(neste caso, é a variavel "resultado" obtido na nossa função).

```
				document.getElementById('resultado').value = resultado;
```


## Built With

* [Bootstrap - cdn](https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css) - Framework web
* [HTML](#) - Linguagem de marcação
* [Javascript](#) - Linguagem de programação web


## Authors

* **Fabrício Rocha** - *Web Developer* - [Perfil github](https://github.com/Developer-Rocha)



