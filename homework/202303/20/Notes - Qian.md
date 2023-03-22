# Given two strings A and B. Find the least repeated times of A to make B as A's substring.
```
public int repeatedStringsMatch(String A, String B) {
    String tempS = A;
    count = 1;
    while(tempS.length < B.length) {
        count += 1;
        tempS += A;
    }
    
    if (tmepS.index(B)) {
      return count;
    }
    count += 1;
    tempS += A;
    
    if (tmepS.index(B)) {
      return count;
    }
    return -1;
}
```
