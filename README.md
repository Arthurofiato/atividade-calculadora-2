  GNU nano 6.2                                                                                       calc.sh                                                                                                
#!/bin/bash

echo "Digite o primeiro número:"
read num1

echo "Digite o segundo número:"
read num2

echo "Escolha a operação a ser realizada: 1)soma, 2)subtracao, 3)multiplicacao, 4)divisao"
read operacao

if [ "$operacao" = "1" ]; then
    resultado=$((num1 + num2))
    echo "O resultado da soma é $resultado"

elif [ "$operacao" = "2" ]; then
    resultado=$((num1 - num2))
    echo "O resultado da subtração é $resultado"

elif [ "$operacao" = "3" ]; then
    resultado=$((num1 * num2))
    echo "O resultado da multiplicação é $resultado"

elif [ "$operacao" = "4" ]; then
    if [ $num2 -eq 0 ]; then
        echo "Erro: Não é possível dividir por zero."
    elif [ $num1 -eq 0 ]; then
        echo "Erro: O dividendo não pode ser zero."
    else
        resultado=$((num1 / num2))
        echo "O resultado da divisão é $resultado"
    fi

else
    echo "Operação inválida. Por favor, escolha entre soma, subtracao, multiplicacao ou divisao."
fi
