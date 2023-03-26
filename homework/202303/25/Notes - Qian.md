# Singleton

```
public class ParkingLot
{
    private static ParkingLot _instance = null;
    private List<Level> levels;
    private ParkingLot()
    {
        levels = new ArrayList<Level>();
    }
    
    public static ParkingLot getInstance()
    {
        if(_instance == null) 
        {
            _instance = new ParkingLot();
        }
        return _instance;
    }
}
```
