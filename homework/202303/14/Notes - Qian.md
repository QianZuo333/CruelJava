# Strategy Design Pattern
```
interface HandleRequestStrategy
{
    public void handleRequest(ExternalRequest request, List<Elevator> elevators);
}

class RandomHandleRequestsStrategy implements HandleRequestStartegy
{
    public void handleRequests(ExternalRequest request, List<Elevator> elevators)
    {
        Random rand = new Random();
        int n = rand.nextInt(elevators.size());
        elevators.get(n).handleExternalRequest(request);
    }
}

class AlwaysOneElevatorHandleRequestStrategy implements HandleRequestStrategy
{
    public void handleRequest(ExternalRequest request, List<Elevator> elevators)
    {
        elevators.get(0).handleExternalRequest(request);
    }

}

class ElevatorSystem
{
    private HandleRequestStrategy strategy = new HandleRequestStrategy();
    private List<Elevator> elevators = new ArrayList<>();
    
    public void setStrategy(HandleRequestStrategy strategy)
    {
        this.strategy = strategy;
    }
    
    public void handleRequest(ExternalRequest request)
    {
        strategy.handleRequest(request, elevators);
    }
}


```
