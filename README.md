# INHERITANCE-EXAMPLE
package shape_inheritance_ex;

/**
 *
 * @author 1BSCCSA038
 */
abstract class shape{
    public abstract double calculateArea();
}
class circle extends shape{
    private double radius;
    public circle (double radius){
        this.radius=radius;
    }
    @Override
   
    public double calculateArea(){
        return Math.PI*radius*radius;
    }

    

}
class rectangle extends shape{
    private double length,width;
    public rectangle(double length,double width){
        this.length=length;
        this.width =width;
    }
    @Override
    public double calculateArea(){
        return length*width;
    }
}
class square extends shape{
    private double side;
    public square(double side){
        this.side=side;
    }
    @Override
    public double calculateArea(){
        return side*side;
    }
}
class triangle extends shape{
    private double base,height;
    public triangle(double base,double height){
        this.base=base;
        this.height=height;
    }
    @Override
    public double calculateArea(){
        return 1.5*base*height;
    }
}

public class Shape_inheritance_ex {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        shape Circle=new circle(3);
        shape Rectangle = new rectangle(3,6);
        shape Square=new square(8);
        shape Triangle =new triangle(3,6);
        
        System.out.println("Circle Area:"+Circle.calculateArea());
        System.out.println("Rectengle Area:"+Rectangle.calculateArea());
        System.out.println("Square Area:"+Square.calculateArea());
        System.out.println("Triangle Area:"+Triangle.calculateArea());
    }
    
}


o/p:
Circle Area:28.274333882308138
Rectengle Area:18.0
Square Area:64.0
Triangle Area:27.0
