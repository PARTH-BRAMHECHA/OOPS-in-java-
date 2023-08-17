
// Java program to add two complex numbers
 import java.util.Scanner;
class Complex {
 //declaration of variables
     float real, imag;
     
 //constructor fuction
    public Complex(float r, float i)
    {
        this.real = r;
        this.imag = i;
    }
 
    //function to print a number
    public void print()
    {
        System.out.println(this.real + " +i" + this.imag);
    }
 
    // function for addition
    public static Complex add(Complex n1,Complex n2)
    {
         Complex res = new Complex(0, 0);
 
        // adding real parts of both complex numbers
        res.real = n1.real + n2.real;
 
        // adding imaginary parts
        res.imag = n1.imag + n2.imag;
 
        // returning result
        return res;
    }
    
    //function for subtraction
        public static Complex sub(Complex n1,Complex n2)
    {
         Complex res = new Complex(0, 0);
 
        // adding real parts of both complex numbers
        res.real = n1.real - n2.real;
 
        // adding imaginary parts
        res.imag = n1.imag - n2.imag;
 
        // returning result
        return res;
    }
    
        //function for multiplication
        public static Complex mul(Complex n1,Complex n2)
    {
         Complex res = new Complex(0, 0);

        res.real = (n1.real*n2.real - n1.imag*n2.imag);

        res.imag = n1.real*n2.imag + n1.imag*n2.real;
 
        // returning result
        return res;
    }
    
        //function for division
        public static Complex div(Complex n1,Complex n2)
    {
         Complex res = new Complex(0, 0);

        res.real = (n1.real*n2.real - n1.imag*n2.imag)/(n2.real*n2.real+n2.imag*n2.imag);
 
       res.imag = (n1.imag*n2.real - n1.real*n2.imag)/(n2.real*n2.real+n2.imag*n2.imag);
 
        // returning result
        return res;
    }
 
    public static void main(String arg[])
    {
        //Taking input of the two complex number using scanner
        // creating two complex numbers
        Scanner sc = new Scanner(System.in);
        Complex res;
        float a,b,c,d;
        System.out.print("Enter the real part of the first number\n");
        a=sc.nextFloat();
        System.out.println("Enter the imaginary part of the first number");
        b=sc.nextFloat();
        System.out.println("Enter the real part of the second number");
        c=sc.nextFloat();
        System.out.println("Enter the imaginary part of the second number");
        d=sc.nextFloat();
        
        //making objects
        Complex c1 = new Complex(a,b);
        Complex c2 = new Complex(c,d);
 
       // calling add() to perform addition
         res = add(c1, c2);
         // displaying addition
        System.out.println("\nAddition is :");
        res.print();
        
        // calling sub() to perform subtraction
         res = sub(c1,c2);
         // displaying addition
        System.out.println("\nSubtraction :");
        res.print();
        
        // calling mul() to perform addition
         res = mul(c1, c2);
         // displaying multiplication
        System.out.println("\nMultiplication is :");
        res.print();
        
        // calling div()) to perform division
         res = add(c1, c2);
         // displaying division
        System.out.println("\nDivision is :");
        res.print();
    }
}   
