# Function-in-CPP
C++ Functions. A function is a block of code which only runs when it is called. You can pass data, known as parameters, into a function. Functions are used to perform certain actions, and they are important for reusing code: Define the code once, and use it many times.

//1.To declare prototype of the function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

int main()
{
 float sum(int ,float); //function pototype
 
 int a=20;
 float s,b=2.5;
 s=sum(a,b);
 cout<<"Sum="<<s;
 return 0;
 }
 
 float sum(int x,float y)
 {
  retun(x+y);
 }
 
 =====================================
 
 //2.To declare and define void function
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 #include<iostream>
 using namespace std;
 
 int main()
 {
   void show(void);
   show();
   return 0;
 }
 
 void show()
 {
  cout<<"\n In show();
  }
  
  ====================================
  
  //3.To demonstrate call by value
  ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  
  #include<iostream>
  using namespace std;
  
  int main()
  {
  int x,y;
  void swap(int ,int);
  cout<<"\n Enter the values of x & y);
  cin>>x>>y;
  swap(x,y); //function call
  cout<<"\n In function main<<endl;
  cout<<"\n Address x="<<(unsigned)&x << "and y="<<(unsigned)&y;
  return 0;
  }
  
  void swap(int a,int b)
  {
   int k;
   k=a;
   b=k;
   cout<<"In swap Function"<<endl;
   cout<<"\n values of x="<<a<<"Values of y="<<b;
   cout<<"\n Address x="<<(unsigned)&a << "and y="<<(unsigned)&b;
   }
   
   ====================================================
   
   //4.Call by address
   ~~~~~~~~~~~~~~~~~~~~~~
   
   #include<iostream>
   using namespace std;
   
   int main()
  {
  int x,y;
  void swap(int * ,int *);
  cout<<"\n Enter the values of x & y);
  cin>>x>>y;
  swap(&x,&y); //function call
  cout<<"\n In function main<<endl;
  cout<<"\n Address x="<<(unsigned)&x << "and y="<<(unsigned)&y;
  return 0;
  }
  
  void swap(int *a,int *b)
  {
   int *k;
   *k=*a;
   *b=*k;
   cout<<"In swap Function"<<endl;
   cout<<"\n values of x="<<*a<<"Values of y="<<*b;
   cout<<"\n Address x="<<(unsigned)&a << "and y="<<(unsigned)&b;
   }
   
   ============================
   
   //5.pass by address,value,reference
   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   #include<iostream
   using namespace std;
   
   int main()
   {
    void funA(int s);
    void funB(int &);
    void funC(int *);
    int s=4; //initial value
    funA(s); //s passed by value
    cout<<"\n Value of s="<<s<<"Address of s="<<unsigned(&s);
    funB(s); //pass by reference
    cout<<"\n Value of s="<<s<<"Address of s="<<unsigned(&s);
    funC(s); // pass by address(in C mode)
    cout<<"\n Value of s="<<s<<"Address of s="<<unsigned(&s);
    return 0;
    }
    
    void funA(int i)
    { i++; }
    
    void funB(int &k)
    { k++; }
    
    void func(int *j)
    { j++; }
    
    ===============================
    
    //6.Demonstrate call by reference
    
    #include<iostream>
    using namespace  std;
    
    int main()
    {
      int x,y;
      void swap(int &,int &)
      cout<<"\n Enter the values of x & y);
      cin>>x,y;
      swap(x,y);
      cout<<"\n In main()";
      cout<<"\n Values of x="<<x<<"Value of y="<<y;
      cout<<"\n Address of x="<<unsigned(&x)<<"Address of y="<<y<<endl;
      return 0;
    }
    
    void swap(int &a,int &b)
    {
       int k;
       k=a;
       a=b;
       b=k;
       cout<<"\n In swap()"<<end;
       cout<<"\n Values of x="<<x<<"Value of y="<<y;
       cout<<"\n Address of x="<<unsigned(&x)<<"Address of y="<<y<<endl;
          
    }
    
    ============================================
    
    //7.To retun a value by reference
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    
    #include<iostream>
    using namespace std;
    int main()
    {
      int &min(int &j,int &k)
      int a=18,b=11,c;
      c=min(a,b);
      cout<<"Minimum value="<<c;
      return 0;
    }
    
    int &min(int &j,int &k)
    {
       if(k<j)
       return k;
       
       else
       return j;
     }
     
     ===========================

//8.To demonstrate return by reference
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

int main()
{
  int & large(int &p,int &q);
  int l,k;
  cout<<"\n Enter the value of L & K";
  cin>>l>>k;
  large(l,k)=120;
  cout<<"l="<<l<<"k="<<k;
  return 0;
}

int & large(int &p,int &q)
{
  if(p>q)  return p;
  else q;
}

=============================

//9.Returning more value by Reference
#include<iostream>
using namespace std;

int main()
{
int sq,cb,n;
void more(int &,int & ,int);
cout<<"\n Enter a Number";
cin>>n;
more(sq,cb,n);
cout<<"\n Square="<<sq;
cout<<"\n Cube="<<cb;
return 0;
}

void more(int & s,int & c,int j)
{
 s=J*j;
 s=j*j;
}

===================

//10.

     
    
      
   

    
    
    
   
   
   
  
   
