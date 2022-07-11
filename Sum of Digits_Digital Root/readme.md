## Digital root is the recursive sum of all the digits in a number. Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. The input will be a non-negative integer.
## Examples:
```java
    16  -->  1 + 6 = 7
   942  -->  9 + 4 + 2 = 15  -->  1 + 5 = 6
132189  -->  1 + 3 + 2 + 1 + 8 + 9 = 24  -->  2 + 4 = 6
493193  -->  4 + 9 + 3 + 1 + 9 + 3 = 29  -->  2 + 9 = 11  -->  1 + 1 = 2
```
## Solution:
```java
public class DRoot {
  public static int digital_root(int n) {
    String digits = String.valueOf(n);
    int sum = 0;
    for(int i=0;i<digits.length();i++){
      sum+=Character.getNumericValue(digits.charAt(i));
      System.out.println(sum);
    }
    if(sum < 10){
      return sum;
    }
    return digital_root(sum);
  }
}
```
