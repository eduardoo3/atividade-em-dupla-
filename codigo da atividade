#include <iostream>
#include <string>
#include <vector>

struct Usuario {
    std::string nome;
};
//cadastro de menu
void exibirMenu() {
    std::cout << "Menu de Opções:\n";
    std::cout << "1. Cadastrar frutas favoritas\n";
    std::cout << "2. Exibir Lista\n";
    std::cout << "3. Sair do Sistema\n";
    std::cout << "Escolha uma opção: ";
}
//solicitaçao do nome de usuario
int main() {
    std::vector<Usuario> usuarios;
    int opcao;

    std::string nomeUsuario;
    std::cout << "Por favor, insira seu nome: ";
    std::getline(std::cin, nomeUsuario);
    std::cout << "Bem-vindo(a), " << nomeUsuario << "!" << std::endl;

    std::vector<std::string> frutas;

    do {
        exibirMenu();
        std::cin >> opcao;
        std::cin.ignore(); 
// solicitaçao da lista de frutas 
        switch (opcao) {
            case 1: {
                std::string fruta;
                std::cout << "Informe as suas frutas favoritas (digite 'fim' para terminar): ";
                while (true) {
                    std::getline(std::cin, fruta);
                    if (fruta == "fim") break;
                    frutas.push_back(fruta);
                }
                break; 
            }
//exibiçao da lista de frutas favoritas
            case 2: {
                std::cout << "\nLista de frutas favoritas\n";
                if (frutas.empty()) {
                    std::cout << "Nenhuma fruta cadastrada.\n";
                } else {
                    for (const auto& fruta : frutas) {
                        std::cout << "Fruta favorita: " << fruta << "\n";
                        std::cout << "-----------------------------\n";
                    }
                }
                break;
            }

            case 3: {
                std::cout << "Saindo do sistema...\nAté logo, " << nomeUsuario << "!\n";
                break;
            }

            default: {
                std::cout << "Opção inválida! Tente novamente.\n";
                break;
            }
        }
        std::cout << std::endl;
    } while (opcao != 3);

    return 0;
}
