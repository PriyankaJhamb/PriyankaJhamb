Here is the example that I have run and find the answer different:
```
str="priyanka";
cout<<"str.substr(0, 0): "<<str.substr(0, 0)<<endl; //
cout<<"str.substr(0, 3): "<<str.substr(0, 3)<<endl; // pri
cout<<"str.substr(1, 4): "<<str.substr(1, 4)<<endl; // riya
cout<<"str.substr(1, 1): "<<str.substr(1, 1)<<endl; // r
```
`When starting index is (0, 0) , then it is giving me nothing but when I have index(1,1) or any positive index except 0, it is giving me the index character.`

`Similarly, when index(0, 3) is given, it has started from 0 to 2 only, not last index 3 but when index(1, 4) is given, it has started from 1 and end at 4.`



## One more thing is"
```
cout<<"str.substr(0, -5): "<<str.substr(0, -5)<<endl;
```
it will print whole string if end index will be negative.

and 
```
cout<<"str.substr(-1, 5): "<<str.substr(-1, 5)<<endl;
``` 
it will gives an error of out of range if starting index is negative 
i.e 
terminate called after throwing an instance of 'std::out_of_range'
  what():  basic_string::substr: __pos (which is 18446744073709551615) > this->size() (which is 8)
Aborted (core dumped)
  
 
