#include <iostream>   
using namespace std;

int f(int x) {
宣告函式的宣輸入參數並回傳
    if (x == 0 || x == 1) {
如果x=0或者x =1
        return x + 1;
返回x+1
    }
    else if (x > 1) {
如果x>1
        return f(x - 1) + f(x / 2);
返回f(x-1)+f(x / 2)
    }
}

int main() {  
    int x;
宣告整數
    cin >> x;
輸入整數
    cout << f(x) << "\n";
輸出函式的值
    return 0;
}
