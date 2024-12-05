def selection_sort(arr):
    """
    Ordena uma lista usando o algoritmo Selection Sort.

    :param arr: Lista de elementos a serem ordenados.
    :return: A lista ordenada.
    """
    n = len(arr)

    for i in range(n):
        # Encontra o índice do menor elemento no subarray [i...n-1]
        min_idx = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j

        # Troca o menor elemento encontrado com o primeiro elemento não ordenado
        arr[i], arr[min_idx] = arr[min_idx], arr[i]

    return arr


# Testes
if __name__ == "__main__":
    data = [64, 25, 12, 22, 11]
    print("Lista original:", data)
    sorted_data = selection_sort(data)
    print("Lista ordenada:", sorted_data)

# 7.-Selection-Sort
