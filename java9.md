```cpp
#include <iostream>
#include <list>
using namespace std;

int main() {
    list<int> l1;
    int input;
    
    for (int i = 0; i<=5; i++){
        fillimi:
        cin >> input;
        if (input%2!=0){
            if (input == 5){
                continue;
            }
            if (input == 9){
                break;
            }
            l1.push_back(input);
        }
        else{
            cout << "\nShtyp numer tek!";
            goto fillimi;
        }
    }
    /*
        for (int i: l1){
            cout << i << " ";
        }
    */
    
    list<int>::iterator itr;
    for (itr = l1.begin();itr != l1.end(); ++itr){
        cout << *itr <<" ";
    }
    
    /*
Të provohen të gjitha metodat më poshtë    
    1.swap
    2.insert
    3.erase
    4.find
    6.next
    7.advance
    8.unique
    9.sort
    10.reverse
    11.splice!!
    12.begin
    13.end	
    14.rbegin	
    15.rend	
    16.cbegin
    17.cend	
    18.crbegin	
    19.crend
    */

    return 0;
}
```
