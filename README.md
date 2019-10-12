# Military-Equipment-Class-Algorithm



import java.io.*;

public class MilitaryEquip

{

public String name;

public int quantity;

MilitaryEquip(String name, int n)

{

this.name=name;

this.quantity=n;

}

void display() throws IOException

{

System.out.println("Name: "+this.name);

System.out.println("Quan: "+this.quantity);

}

public static void main(String [] args)

{

try{

MilitaryEquip e1=new MilitaryEquip1("Equip1",11,"Bullets");

e1.display();

MilitaryEquip e2=new MilitaryEquip2("Equip2",22,"1000");

 e2.display();

 MilitaryEquip e3=new MilitaryEquip3("Equip3",33,"150kg");

 e3.display();

}

catch(Exception e)

{

System.out.println("In BASE CLASS");

System.out.println(e);

}

}

}

 

class MilitaryEquip1 extends MilitaryEquip

{

public String category;

public MilitaryEquip1(String name,int n ,String cat)

{

super(name,n);

this.category=cat;

}

void display() throws IOException

{

super.display();

System.out.println("Cat: "+this.category);

System.out.println("In SUB CLASS:1");

BufferedReader read=new BufferedReader(new FileReader("hello.txt"));

}

}

 

class MilitaryEquip2 extends MilitaryEquip

{

public String capacity;

public MilitaryEquip2(String name,int n ,String cap)

{

super(name,n);

this.capacity=cap;

}

void display() throws IOException

{

super.display();

System.out.println("Cat: "+this.capacity);

System.out.println("In SUB CLASS :2");

//BufferedReader read=new BufferedReader(new FileReader("hello.txt"));

}

}

 

class MilitaryEquip3 extends MilitaryEquip

{

public String weight;

public MilitaryEquip3(String name,int n ,String w)

{

super(name,n);

this.weight=w;

}

void display() throws IOException

{

super.display();

System.out.println("Cat: "+this.weight);

System.out.println("In SUB CLASS :3");

//BufferedReader read=new BufferedReader(new FileReader("hello.txt"));

}

}

