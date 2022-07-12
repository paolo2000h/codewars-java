## Given an array (arr) as an argument complete the function countSmileys that should return the total number of smiling faces. Rules for a smiling face:
* Each smiley face must contain a valid pair of eyes. Eyes can be marked as : or ;
* A smiley face can have a nose but it does not have to. Valid characters for a nose are - or ~
* Every smiling face must have a smiling mouth that should be marked with either ) or D
## Examples:
```java
countSmileys([':)', ';(', ';}', ':-D']);       // should return 2;
countSmileys([';D', ':-(', ':-)', ';~)']);     // should return 3;
countSmileys([';]', ':[', ';*', ':$', ';-D']); // should return 1;
```
## Solution:
```java
import java.util.*;

public class SmileFaces {
  
  public static int countSmileys(List<String> arr) {
      return (int) arr.stream().filter(a -> a.matches("[:;][-~]?[)D]")).count();
  }
}
```
