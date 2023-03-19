include<iostream> //引入 C++ 的標準輸入輸出庫
using namespace std; //命名空間 std，簡化後面的程式碼

int main() //主函數的開始
{
    int a, b, t; //定義三個整數變數

    while( cin >> a >> b ) //循環讀入 a 和 b 的值，當標準輸入結束時停止循環
    {
        while( b!=0 ) //當 b 不等於 0 時進入循環
        {
            t = b; //用變數 t 暫存 b 的值
            b = a%b; //用 a 對 b 取餘數，把結果存入 b 中
            a = t; //用 t 的值更新 a 的值
        }
        cout << a << endl; //輸出 a 的值，並換行
    }

    return 0; //回傳 0，表示程式正確結束
}
