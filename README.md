#include <iostream>

using namespace std;

int main() {
    int num_items;
    cout << "Enter the number of array items: ";
    cin >> num_items;

    int array[num_items];
    cout << "Enter array items: ";
    for (int i = 0; i < num_items; ++i) {
        cin >> array[i];
    }

    string rotation_direction;
    cout << "Enter rotation direction (left or right): ";
    cin >> rotation_direction;

    int num_cells;
    cout << "Enter the number of cells to rotate: ";
    cin >> num_cells;

    int n = num_items;
    int rotated_array[n];

    for (int i = 0; i < n; ++i) {
        int rotated_index = (rotation_direction == "right") ? (i + num_cells) % n : (i + n - num_cells) % n;
        rotated_array[rotated_index] = array[i];
    }

    cout << "Rotated Array: ";
    for (int i = 0; i < n; ++i) {
        cout << rotated_array[i] << " ";
    }
    cout << endl;

    return 0;
}
    
    
