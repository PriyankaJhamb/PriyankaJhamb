
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
![image](https://user-images.githubusercontent.com/74251229/151370865-df75b047-925b-4ba5-8744-1a28514b5865.png)

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
![image](https://user-images.githubusercontent.com/74251229/151370911-198c1b99-5c03-4eb5-82df-b1a013130318.png)


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
![image](https://user-images.githubusercontent.com/74251229/151370944-7a311d40-c2dd-4d27-a558-02706571f05c.png)

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
![image](https://user-images.githubusercontent.com/74251229/151370971-de765a73-f70e-459e-a976-21cad47a5477.png)

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
![image](https://user-images.githubusercontent.com/74251229/151371009-11c7960e-1a03-4199-9325-34ac7c2ce8c8.png)


## Differnce in tabular form


|  cin | cin.getline() |
|------|---------------|
| When it encounters space, tab or new line, it stops to take input into the buffer for particular variable. | It stops when it encounters optional delimiter. By default, optional delimiter is new line '\n'. |
| It does not take any argument. | It takes an argument of length which we can give any but less than (variable_array_length +1) only. |
| cin is basically an object in C++ of the class istream that accepts input from the standard input device. | getline is a standard library function that is used to input a string or reads a line from input stream |






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


## References Section:
[https://pediaa.com/](https://pediaa.com/what-is-the-difference-between-getline-and-cin/#:~:text=The%20main%20difference%20between%20getline,an%20instance%20of%20istream%20class.&text=Each%20header%20file%20has%20functions,these%20functions%20in%20their%20programs.)

