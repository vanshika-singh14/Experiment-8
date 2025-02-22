# Experiment-8
## Aim:
To study and implement C++ 2D Array - Matrices
## Theory:

A 2D array in C++ can be defined as a data structure that deals with two-dimensional grid formats such as matrices wherein every single element is well identified by two indices: one for rows and another one for columns. It is similar to an array composed of other arrays.

A two-dimensional array could be declared using the syntax type arrayName[rows][columns]; For instance, int matrix[3][4]; indicates three rows by four columns. All its members occupy successive positions in memory meaning they are laid out linearly following row-major order scheme hence it makes it different from accessing them through single index only but rather via two indexes.They may be initialized while being declared. For static arrays they require listing down values enclosed in nested braces whereas dynamic arrays size calculation occurs at run-time stage hence this involves dynamic allocation using new’s keyword and deallocation using delete’s keyword in C++.Elements can be accessed using their respective row and column indexes. The iteration uses mostly a two-fold loop: the outer one is run for rows while the inner one does columns. It enables you to treat or manipulate one element of an entire array.

## Code:
a)
# include<iostream>
using namespace std;
int main()
{
    //matrix input and display
    int a[2][2];
    int i,j;
    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }

    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }

}

b)
# include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int b[2][2];
    int s[2][2];
    int i,j,r = 0,c=0;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            s[i][j] = a[i][j] + b[i][j];
        }
    }

    cout<<"Sum: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<s[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
c)
# include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0,s = 0;
    int a[r][c];
    int b[r][c];
    int p[r][c];
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
for (int i = 0; i < r; ++i) 
{
        for (int j = 0; j < r; ++j) 
        {
            p[i][j] = 0;
            for (int k = 0; k <c; ++k) 
            {
                p[i][j] += a[i][k] * b[k][j];
            }
        }
}

    cout<<"Product: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<p[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
d)
# include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0;
    int a[r][c];
    int da = 0;
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int i = 0; i < r; i++) 
    {
        da = da + a[i][i];
    }

cout<<"Diagonal Sum: "<<da<<endl;


}
e)
# include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int i,j,r = 0,c=0;
    bool eqr = true;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int j = 0; j < c; j++) 
    {
        if (a[0][j] != a[1][j]) 
        {
            eqr = false;
            break;
        }
    }
    cout<<"Row equality: "<<eqr;
}

Output:
a) ![image](https://github.com/user-attachments/assets/39e3693d-d786-4e3e-be74-b60fb42da200)
b)![image](https://github.com/user-attachments/assets/470ba2ff-4471-43d4-b596-0959bc024f2d)
c)![image](https://github.com/user-attachments/assets/d35f90a9-d18f-49c3-8759-2ca9f6caed28)
d)![image](https://github.com/user-attachments/assets/6475a3fa-f0a7-4651-aba2-b32d493772dc)
e)![image](https://github.com/user-attachments/assets/2d49225c-d94c-4997-8b9d-2732d580043a)



