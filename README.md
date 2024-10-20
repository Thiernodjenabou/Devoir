# Devoir

#include <iostream>
#include <vector>

template<typename... Args>
void testFunction(Args... args) {
    // Fonction vide pour tester le nombre d'arguments
}

int main() {
    int count = 0;

    while (true) {
        // Prépare un tableau d'arguments
        std::vector<int> args(count, 0); // Tous les arguments sont des zéros

        if (count > 0) {
            // Appelle la fonction avec le bon nombre d'arguments
            testFunction(args.data(), args.size()); // Appel avec un tableau de taille variable

            std::cout << "Nombre de paramètres testés : " << count << std::endl; // Affiche le nombre de paramètres
        }

        count += 1; // Augmente le nombre de paramètres de 1 à chaque itération
    }

    return 0;
}
