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

O - Open close principle, 

L - Liskov substitution principle

I - Interface segregation principle

D - Dependency inversion principle


