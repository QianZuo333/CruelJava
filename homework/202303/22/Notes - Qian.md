```
import java.util.concurrent.ConcurrentHashMap;

public class Example {
    private static ConcurrentHashMap<String, Integer> map = new ConcurrentHashMap<>();

    public static void main(String[] args) {
        // Create and start multiple threads to add values to the map
        for (int i = 0; i < 10; i++) {
            new Thread(() -> {
                for (int j = 0; j < 1000; j++) {
                    addValue("key", 1);
                }
            }).start();
        }

        // Wait for all threads to complete
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        // Print the final value in the map
        System.out.println("Final value: " + map.get("key"));
    }

    private static void addValue(String key, int value) {
        // Use the putIfAbsent method to add the key-value pair if it doesn't exist
        // If the key already exists, use the compute method to update the value
        map.compute(key, (k, v) -> (v == null) ? value : v + value);
    }
}

```
