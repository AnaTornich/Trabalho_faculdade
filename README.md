# Trabalho_faculdade
trabalho de Linguagem de programação

Ana Beatriz Silva Tornich

Lista de Exercícios 

1- Calculadora Simples
Crie uma classe Calculadora com métodos para as quatro operações básicas (soma, subtração, multiplicação, divisão). O programa principal deve permitir ao usuário inserir dois números e escolher a operação desejada. Exiba o resultado.

#include <iostream>
using namespace std;

// Classe Calculadora
class Calculadora {
public:
    double somar(double a, double b) {
        return a + b;
    }

    double subtrair(double a, double b) {
        return a - b;
    }

    double multiplicar(double a, double b) {
        return a * b;
    }

    double dividir(double a, double b) {
        if (b == 0) {
            cout << "Erro: Divisão por zero!\n";
            return 0;
        }
        return a / b;
    }
};

int main() {
    Calculadora calc;
    double num1, num2;
    int opcao;

    cout << "=== CALCULADORA SIMPLES ===\n";
    cout << "Digite o primeiro número: ";
    cin >> num1;

    cout << "Digite o segundo número: ";
    cin >> num2;

    cout << "\nEscolha a operação:\n";
    cout << "1. Soma\n";
    cout << "2. Subtração\n";
    cout << "3. Multiplicação\n";
    cout << "4. Divisão\n";
    cout << "Opção: ";
    cin >> opcao;

    cout << "\nResultado: ";

    switch (opcao) {
        case 1:
            cout << calc.somar(num1, num2) << endl;
            break;
        case 2:
            cout << calc.subtrair(num1, num2) << endl;
            break;
        case 3:
            cout << calc.multiplicar(num1, num2) << endl;
            break;
        case 4:
            cout << calc.dividir(num1, num2) << endl;
            break;
        default:
            cout << "Opção inválida!" << endl;
    }

    return 0;
}

