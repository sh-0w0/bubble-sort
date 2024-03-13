#include <stdio.h>

void bubbleSort(int arr[], int n) {
    int i, j;
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int tmp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = tmp;
            }
        }
    }
}

void printArray(int arr[], int size) {
    int i;
    for (i = 0; i < size; i++)
        printf("%d ", arr[i]);
    printf("\n");
}

int main() {
    int arr[100];
    int n;

    printf("입력 개수 : ");
    scanf_s("%d", &n);

    for (int i = 0; i < n; i++)
        scanf_s("%d", &arr[i]);

    printf("\n\n");

    printf("정렬 전: \n");
    printArray(arr, n);

    bubbleSort(arr, n);

    printf("정렬 후: \n");
    printArray(arr, n);

    return 0;
}
