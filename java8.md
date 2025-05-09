## Algoritmet dhe Strukturat e të Dhënave – Java 8


**Detyra 1:**
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<int> IntQueue;
    int shuma = 0;
    for (int i = 1; i<=10; i+=2){
        IntQueue.push (i);
    }
    
    while (!IntQueue.empty()){
        cout << "\nMadhesia e IntQueue eshte: " << IntQueue.size();
        cout << "\nNe fillim te IntQueue eshte: " << IntQueue.front();
        cout << "\nNe fund te IntQueue eshte: " << IntQueue.back();
        shuma = shuma + IntQueue.front();
        IntQueue.pop();
        }
        
        cout << "\nShuma: " << shuma;

    
    
    return 0;
}
```
**Detyra 2:**
```cpp
void paraswap(queue <char> q1,queue <char> q2) {
	for (int i = 'A';i <= 'D';i++) {
		q1.push(i);
	}
	for (int i = 'a';i <= 'd';i++) {
		q2.push(i);
	}
	cout << "Antaret e queue 1 para swap:" << endl;
	while (!q1.empty()) {
		cout << q1.front() << endl;
		q1.pop();
	}
	cout << endl << endl;
	cout << "Antaret e queue 2 para swap:" << endl;
	while (!q2.empty()) {
		cout << q2.front() << endl;
		q2.pop();
	}
	cout << endl << endl;
}
void passwap(queue <char> q1, queue <char> q2) {
	for (int i = 'A';i <= 'D';i++) {
		q1.push(i);
	}
	for (int i = 'a';i <= 'd';i++) {
		q2.push(i);
	}
	q1.swap(q2);
	cout << "Antaret e queue 1 pas swap:" << endl;
	while (!q1.empty()) {
		cout << q1.front() << endl;
		q1.pop();
	}
	cout << endl << endl;
	cout << "Antaret e queue 2 pas swap:" << endl;
	while (!q2.empty()) {
		cout << q2.front() << endl;
		q2.pop();
	}
	cout << endl << endl;
}
int main() {
	queue <char> q1;
	queue<char> q2;
	paraswap(q1,q2);
	passwap(q1, q2);
}
```
**Detyra 3:** Duke perdorur emplace() ne priority queue te tipit string, te ruhen vlerat "Kolokviumi i pare ne ASDh mbahet me 22 Prill" dhe "Kolokviumi i pare ne ASDh mbahet me 29 Prill". Ne fund, te shfaqet dhe analizohet rezultati i fituar.
**Detyra 4:**
```cpp
#include <iostream>
#include <list>
using namespace std;

int main()
{
	// defining list
	list<int> gqlist{12,45,8,6};

	for (auto i : gqlist) {
		cout << i << ' ';
	}
	return 0;
}
```
---

**Detyra 5:**
```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {

    // create a list
    list<int> numbers = {1, 2, 3, 4, 5};
  
    // display the first element
    cout << "First Element: " << numbers.front() << endl;
  
    // display the last element
    cout << "Last Element: " << numbers.back();
  
    return 0;
}
```
---

**Detyra 6:**
```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {
    
    // create a list
    list<int> numbers = {1, 2, 3};
  
    // display the original list 
    cout << "Initial List: ";
    for(int number: numbers) {
        cout << number << ", ";
    }
  
    // add element at the beginning
    numbers.push_front(0);

    // add element at the end
    numbers.push_back(4);

    // display the modified list
    cout << endl << "Final List: ";
    for(int number : numbers) {
        cout << number << ", ";
    }

  return 0;

}

```
---

**Detyra 7:**
```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {

    // create the list
    list<int> numbers {1, 2, 3, 4};
  
    // display the elements of the list
    cout << "List Elements: ";
    for(int number : numbers) {
        cout << number <<", ";
    }
    
    return 0;

}
```
---

**Detyra 8:**
```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {

     // create a list
    list<int> numbers = {1, 2, 3, 4, 5};

    // create an iterator to point to the first element of the list
    list<int>::iterator itr = numbers.begin();
  
    // increment itr to point to the 2nd element
    ++itr;
    
    //display the 2nd element
    cout << "Second Element: " << *itr << endl;
  
    // increment itr to point to the 4th element
    ++itr;
    ++itr;

    // display the 4th element
    cout << "Fourth Element: " << *itr;
  
    return 0;
}
```
---

**Detyra 9:**
```cpp
#include <iostream>
#include <iterator>
#include <list>
using namespace std;

// function for printing the elements in a list
void showlist(list<int> g)
{
	list<int>::iterator it;
	for (it = g.begin(); it != g.end(); ++it)
		cout << '\t' << *it;
	cout << '\n';
}

int main()
{

	list<int> gqlist1, gqlist2;

	for (int i = 0; i < 10; ++i) {
		gqlist1.push_back(i * 2);
		gqlist2.push_front(i * 3);
	}
	cout << "\nList 1 (gqlist1) is : ";
	showlist(gqlist1);

	cout << "\nList 2 (gqlist2) is : ";
	showlist(gqlist2);

	cout << "\ngqlist1.front() : " << gqlist1.front();
	cout << "\ngqlist1.back() : " << gqlist1.back();

	cout << "\ngqlist1.pop_front() : ";
	gqlist1.pop_front();
	showlist(gqlist1);

	cout << "\ngqlist2.pop_back() : ";
	gqlist2.pop_back();
	showlist(gqlist2);

	cout << "\ngqlist1.reverse() : ";
	gqlist1.reverse();
	showlist(gqlist1);

	cout << "\ngqlist2.sort(): ";
	gqlist2.sort();
	showlist(gqlist2);

	return 0;
}
```
---

**Detyra 10:**
```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {
    // create a list
    list<int> numbers = {1, 2, 3, 4, 5};
 
    // display the original list 
    cout << "Inital List: ";
    for(int number : numbers) {
        cout << number << ",  ";
    }

    // remove the first element of the list
    numbers.pop_front();

    // remove the last element of the list
    numbers.pop_back();

    // display the modified list 
    cout << endl << "Final List: ";
    for(int number : numbers) {
        cout << number << ", ";
    }

    return 0;
}
```
---

**Detyra 11:**
```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {
    // create a list
    list<int> numbers = {1, 2, 3, 4, 5};
 
    // display the original list 
    cout << "Inital List: ";
    for(int number : numbers) {
        cout << number << ",  ";
    }

    // remove the first element of the list
    numbers.pop_front();

    // remove the last element of the list
    numbers.pop_back();

    // display the modified list 
    cout << endl << "Final List: ";
    for(int number : numbers) {
        cout << number << ", ";
    }

    return 0;
}
```
**Detyra 12:**
```cpp
#include <iostream>
#include <iterator>
#include <list>
using namespace std;

// function for printing the elements in a list
void showlist(list<int> g)
{
	list<int>::iterator it;
	for (it = g.begin(); it != g.end(); ++it)
		cout << '\t' << *it;
	cout << '\n';
}

int main()
{

	list<int> gqlist1, gqlist2;

	for (int i = 0; i < 10; ++i) {
		gqlist1.push_back(i * 2);
		gqlist2.push_front(i * 3);
	}
	cout << "\nList 1 (gqlist1) is : ";
	showlist(gqlist1);

	cout << "\nList 2 (gqlist2) is : ";
	showlist(gqlist2);

	cout << "\ngqlist1.front() : " << gqlist1.front();
	cout << "\ngqlist1.back() : " << gqlist1.back();

	cout << "\ngqlist1.pop_front() : ";
	gqlist1.pop_front();
	showlist(gqlist1);

	cout << "\ngqlist2.pop_back() : ";
	gqlist2.pop_back();
	showlist(gqlist2);

	cout << "\ngqlist1.reverse() : ";
	gqlist1.reverse();
	showlist(gqlist1);

	cout << "\ngqlist2.sort(): ";
	gqlist2.sort();
	showlist(gqlist2);

	return 0;
}
```
