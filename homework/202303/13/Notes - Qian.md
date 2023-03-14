<img width="589" alt="Screen Shot 2023-03-14 at 12 38 18 AM" src="https://user-images.githubusercontent.com/73077953/224929596-bd539811-ae75-4932-84d4-0ec210c76059.png">


```
public class Shape
{
    abstract public float calculateVolumn();
    abstract public float calculateArea();
}

public class Rectangle extends Shape
{
  // Do something
}

public class Cube extends Shape
{
  // Do something
}
```

<img width="594" alt="Screen Shot 2023-03-14 at 12 42 55 AM" src="https://user-images.githubusercontent.com/73077953/224929713-9ba65a56-0611-4299-8d81-86c28eab3343.png">

- Triangle是抽象类；AreaCalculator是具体实现类

```
public class AreaCalculator
{
    private float result;
    private Triangle t;
    
    public float getResult()
    {
        return this.result;
    }
    
    public float calculateArea()
    {
        this.result = t.h * t.b / 2;
    }
}
```
