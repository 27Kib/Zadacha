# Zadacha

#include <iostream>
#include <cstring>
int main() {
    int n;
    std::cout << "Введите количество строк: ";
    std::cin >> n;
    std::cout << "Введите строки:" << std::endl;
    std::string arr[n];
    for (int i = 0; i < n; ++i) {
        std::cin >> arr[i];
    }
    int count = 0;
    for (int i = 0; i < n; ++i) {
        if (arr[i].length() <= 3) {
            ++count;
        }
    }
    if (count == 0) {
        std::cout << "В новом массиве нет строк, удовлетворяющих условиям задачи" << std::endl;
    } else {
        std::string newArr[count];
        int index = 0;
        for (int i = 0; i < n; ++i) {
            if (arr[i].length() <= 3) {
                newArr[index] = arr[i];
                ++index;
            }
        }
        std::cout << "Новый массив из строк:" << std::endl;
        for (int i = 0; i < count; ++i) {
            std::cout << newArr[i] << std::endl;
        }
    }
    return 0;
}

