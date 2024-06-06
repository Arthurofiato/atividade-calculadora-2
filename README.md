#!/bin/bash
echo "Digite o primeiro número:"
read num1
echo "Digite o segundo número:"
read num2
echo "Escolha a operação a ser realizada: soma, subtracao, multiplicacao, divisao"
read operacao
if [ "$operacao" = "soma" ]; then
    resultado=$((num1 + num2))
    echo "O resultado da soma é $resultado"
elif [ "$operacao" = "subtracao" ]; then
    resultado=$((num1 - num2))
    echo "O resultado da subtração é $resultado"
elif [ "$operacao" = "multiplicacao" ]; then
    resultado=$((num1 * num2))
    echo "O resultado da multiplicação é $resultado"
elif [ "$operacao" = "divisao" ]; then
    if [ $num2 -ne 0 ]; then
        resultado=$((num1 / num2))
        echo "O resultado da divisão é $resultado"
    else
        echo "Erro: Não é possível dividir por zero."
    fi
else
    echo "Operação inválida. Por favor, escolha entre soma, subtracao, multiplicacao ou divisao."
fi
