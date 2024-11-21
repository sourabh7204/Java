class Shape
{
int a;

Shape() // default constructor
{
a=0;
}

Shape(int a) // parameterized constructor
{
this.a=a;
}

int side() // method to return side value
{
return(a);
}

void draw()
{
System.out.println("Shape is Drawn");
}

void erase()
{
System.out.println("Shape is Erased");
}

}// end Shape


class Circle extends Shape // sub/derived/child class of Shape
{

Circle()  //default constructor
{
super(); // calls super class default constructor
}

Circle(int r)  // parameterized constructor
{
super(r); // calls super class parameterized constructor
}

void draw() // method overdriding
{
System.out.println("Circle is drawn with radius =" + side());
}

void erase()
{
System.out.println("Circle is Erased");
a=0;
}

}// end Circle

class Triangle extends Shape // sub/derived/child class of Shape
{

int h;

Triangle()  //default constructor
{
super(); // calls super class default constructor
h=0;
}

Triangle(int b, int h)  // parameterized constructor
{
super(b); // calls super class parameterized constructor
this.h=h;
}

void draw()
{
System.out.println("Triangle is drawn with l=" + side() + ", h="+h);
}

void erase()
{
System.out.println("Triangle is Erased");
a=h=0;
}

}// end Triangle


class Square extends Shape // sub/derived/child class of Shape
{

Square()  //default constructor
{
super(); // calls super class default constructor
}

Square(int a)  // parameterized constructor
{
super(a); // calls super class parameterized constructor
}

void draw()
{
System.out.println("Square is drawn with side=" + side());
}

void erase()
{
System.out.println("Square is Erased");
a=0;
}

}// end Square


class ShapeDemo
{
public static void main(String s[])
{
Circle c1= new Circle(5);
Triangle t1=new Triangle(2,3);
Square s1=new Square(6);

c1.draw();
c1.erase();

t1.draw();
t1.erase();

s1.draw();
s1.erase();

System.out.println("Demostrating Polymorphism through dymanic method dispatch");
Shape sh;

sh=c1;
sh.draw();
sh.erase();

sh=t1;
sh.draw();
sh.erase();

sh=s1;
sh.draw();
sh.erase();
} // end main
}// ShapeDemo
