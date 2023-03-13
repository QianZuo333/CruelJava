# S.O.L.I.D Principle
S - Single responsibility principle, the class only has one job.
```
public class AreaCalculator
{
    private float result;
    
    public float getResult()
    {
        return this.result;
    }
    
    public float calculateArea(Triangle t)
    {
        this.result = h * b / 2;
    }
}
```

O - Open close principle, Open to extension, close to modification.
```
public class AreaCalculator
{
    public float calculateArea(Triangle t)
    {
        // Calculates the area for a triangle
    }
    
    public float calculateArea(Rectangle r)
    {
        // Calculates the area for rectangle
    }
}
```
<img width="910" alt="Screen Shot 2023-03-12 at 9 19 30 PM" src="https://user-images.githubusercontent.com/73077953/224607409-764bb846-35c0-45ba-874b-ecdeeba823eb.png">



L - Liskov substitution principle

I - Interface segregation principle

D - Dependency inversion principle


