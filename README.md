#include <iostream>
using namespace std;

int main()
{
    int a, b, count;
    int *num;  // 宣告一個 int 型態的指標變數 num，用來動態分配記憶體
    count = 0;  // 將 count 初始值設為 0
    cin >> a >> b;  // 輸入 a 和 b 的值
    num = new int[a * b];  // 動態分配 a*b 個 int 型態的記憶體，並將起始位址指向 num
    for (int i = 0; i < (a * b); i++)  // 用迴圈將輸入的值存入 num 中
    {
        cin >> num[i];
    }
    for (int i = 0; i < b; i++)  // 用迴圈依序讀取每一列的值
    {
        for (int j = 0; j < a; j++)  // 用迴圈依序讀取每一行的值
        {
            count++;  // 計算目前輸出的元素個數
            cout << num[j * b + i];  // 輸出陣列中的元素
            if (count % a != 0)  // 若不是該列最後一個元素，則輸出一個空格
                cout << " ";
        }
        cout << endl;  // 該列的元素輸出完畢後，換行
    }
    delete[] num;  // 釋放動態分配的記憶體
    return 0;
}
