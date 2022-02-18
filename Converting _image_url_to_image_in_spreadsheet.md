![image](https://user-images.githubusercontent.com/74251229/154684622-d430468d-e618-4bbe-a05c-8331c29c6435.png)

## Using Formula
```
=Image("https://drive.google.com/uc?export=view&id="&mid(A2, 33, 33), 1)
```

#### Actual Url: https://drive.google.com/file/d/1r5h-EN21mLtb8gJrNMgMtXf9pXgEMzCg/
- id in our case: 1r5h-EN21mLtb8gJrNMgMtXf9pXgEMzCg
- mid is the function
- A2 column of url and the 2 is row number
- 33 is the position of starting id in actual url (till 32: https://drive.google.com/file/d/)
- 33 is the length of id
- 1 is mode 

#### if you want to do this for all rows, just drag down after doing for one row, it will automatically take the rows number.

### Reference:
[https://youtu.be/6w7bPSCPHns](https://youtu.be/6w7bPSCPHns)

