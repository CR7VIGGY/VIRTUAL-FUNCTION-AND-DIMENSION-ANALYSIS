# VIRTUAL-FUNCTION-AND-DIMENSION-ANALYSIS
5. Create a base class shape with two double type values and member functions to    input the data and compute_area() for calculating area of figure. Derive two classes’   triangle   and rectangle. Make compute_area() as a virtual function and redefine this   function in the derived class to suit their requirements. Write a program that accepts dimensions of triangle/rectangle and display     calculated area.
//Assgn 4).create a base class Shape with 2 double type value and member function to i/p the data and compute area for calculating area of figure. Derive classes
//TRIANGLE , RECTANGLE , SQUARE ,CIRCLE . Make area as a virtual function and redefine this function on the derived classes to suit their req. . Write  a program
//that accepts dimensions of figure and display calculated area.
//VIGHNESH TIWARI , 4252 , AIT PUNE , INDIA 
//GITHUB PROFILE : CR7VIGGY
#include<bits/stdc++.h>
using namespace std;
class shape
{
	public :
		float x,y;
		virtual void area() = 0;
		void getdata()
		{
			//i/p sides
			cout<<"ENTER THE LENGTH OF SIDES A AND B\n";
			cin>>x>>y;
		}
};
class triangle : public shape
{
	public :
		float z;
		void area()
		{
			z = 0.5*x*y;
			cout<<"AREA : "<<z<<"\n";
		}
};
class rectangle : public shape
{
	public :
		float z;
		void area()
		{
			z = x*y;
			cout<<"AREA : "<<z<<"\n";
		}
};
class  square : public shape
{
	public : 
		float z;
		void area()
		{
			z = x*x;
			cout<<"AREA : "<<z<<"\n";
		}
};
class circle : public shape
{
	public :
		float z;
		void area()
		{
			z = 3.14*x*x;
			cout<<"AREA : "<<z<<"\n";
		}
};

int main()
{
	int i,j,k,m,n;
	shape *p;
	triangle t;
	rectangle r;
	square s;
	circle c;
	do
	{
		cout<<"PRESS 1 : TRIANGLE\nPRESS 2 : RECTANGLE\nPRESS 3 : SQUARE\nPRESS 4 : CIRCLE\nPRESS 5 : EXIT\n";
		cin>>m;
		switch(m)
		{
			case 1 : p = &t;
					 p->getdata();
					 t.area();break;
			case 2 : p = &r;
					 p->getdata();
					 r.area();break;
		    case 3 : p = &s;
					 p->getdata();
					 s.area();break;
			case 4 : p = &c;
					 p->getdata();
					 c.area();break;
		    case 5 : break;
		}
	}
	while(m!=5);
	return 0;
}
