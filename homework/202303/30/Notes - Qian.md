# decorator pattern

```
// The Component interface defines the operations that can be decorated
public interface Component {
    public void operation();
}

// The ConcreteComponent provides the implementation of the Component interface
public class ConcreteComponent implements Component {
    public void operation() {
        System.out.println("ConcreteComponent operation");
    }
}

// The Decorator abstract class implements the Component interface and has a reference to a Component object
public abstract class Decorator implements Component {
    protected Component component;

    public Decorator(Component component) {
        this.component = component;
    }

    public void operation() {
        component.operation();
    }
}

// The ConcreteDecorator adds additional functionality to the Component
public class ConcreteDecorator extends Decorator {
    public ConcreteDecorator(Component component) {
        super(component);
    }

    public void operation() {
        super.operation();
        System.out.println("ConcreteDecorator operation");
    }
}

// The Client uses the Decorator pattern to add additional functionality to the Component
public class Client {
    public static void main(String[] args) {
        Component component = new ConcreteComponent();
        component.operation(); // Output: ConcreteComponent operation

        Component decoratedComponent = new ConcreteDecorator(component);
        decoratedComponent.operation(); // Output: ConcreteComponent operation\nConcreteDecorator operation
    }
}

```
