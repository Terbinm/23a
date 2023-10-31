```java
public abstract class CShape {
    protected String color;
    public abstract void setColor(String str);
    public abstract double getArea();
}

public class CTriangle extends CShape {
    protected double a, b, c;

    public CTriangle(double a, double b, double c) {
        this.a = a;
        this.b = b;
        this.c = c;
    }

    public void setColor(String str) {
        color = str;
    }

    public double getArea() {
        return 0.5 * a * b;
    }

    public void show() {
        System.out.println("color=" + color + ", area=" + getArea());
    }
}

public class Main {
    public static void main(String[] args) {
        CTriangle tri = new CTriangle(3, 4, 5);
        tri.setColor("Red");
        tri.show();
    }
}
```