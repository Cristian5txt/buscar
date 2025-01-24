void buscarNotas(string datos[2][1][1], float notas[2][3]) {
    string nombreBusqueda;
    cout << "Ingrese el nombre para buscar las notas: ";
    cin >> nombreBusqueda;

    bool encontrado = false;

    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 1; j++) {
            for (int k = 0; k < 1; k++) {
                if (datos[i][j][k] == nombreBusqueda) {
                    cout << "Notas de " << nombreBusqueda << ":\n";
                    for (int m = 0; m < 3; m++) {
                        cout << "Nota " << m + 1 << ": " << notas[i][m] << endl;
                    }
                    encontrado = true;
                    break;
                }
            }
            if (encontrado) break;
        }
        if (encontrado) break;
    }

    if (!encontrado) {
        cout << "El nombre no fue encontrado en la lista.\n";
    }
}
