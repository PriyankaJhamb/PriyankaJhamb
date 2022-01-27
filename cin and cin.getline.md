
## Are you confused about using cin and cin.getline both in a single program? 
Let us discuss first what is difference between cin and cin.getline…
Both cin object and cin.getline function are basically used for taking input from the user.
### So, what's difference?
```
cin>>name_of_the_variable;
cin.getline(name_of_the_variable, string_length, optional_delimiter);
```
Example:
```
#include <iostream>
using namespace std;
int main() {
char name[10];
cout<<"Input: ";
cin>>name;
cout<<"Output: "<<name<<endl;
}
```
Output
```
#include <iostream>
using namespace std;
int main() {
char name[10];
cout<<"Input: ";
cin.getline(name, 10);
cout<<"Output: "<<name<<endl;
}
```

Output

### Now Question is why this is happened?
Because cin does not take input after it sees any space, any tab, any new line but cin.getline stops taking input when it sees any delimiter i.e default delimiter is \n (new line).
One more difference is there. let us see example first:)
```
#include <iostream>
using namespace std;
int main() {
char name[10];
cout<<"Input: ";
cin>>name;
cout<<"Output: "<<name<<endl;
}
```
Output
```
#include <iostream>
using namespace std;
int main() {
char name[10];
cout<<"Input: ";
cin.getline(name, 10);
cout<<"Output: "<<name<<endl;
}
```
Output

So, now I hope you have got it: 
so every character array automatically puts '\0' at last index after our string is complete. 
now again sees this when we are putting one more than array size:
```
#include <iostream>
using namespace std;
int main() {
char name[10];
cout<<"Input: ";
cin.getline(name, 11);
cout<<"Output: "<<name<<endl;
}
```
Output
### Simple Program to explain the problems that we usually get into while using both cin and cin.getline
```
#include <iostream>
using namespace std;
int main() {
char name[10], nameother[10];
cin>>name;
cout<<name;
cin.getline(nameother, 10);
cout<<nameother<<endl;
}
```
Firstly, Let us discuss…After we will run this program, what we will found:)
INPUT
Strawberry
