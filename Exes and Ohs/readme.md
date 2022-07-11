## Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.
## Examples:
```java
XO("ooxx") => true
XO("xooxx") => false
XO("ooxXm") => true
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true
XO("zzoo") => false
```
## Solution:
```java
public class XO {
  
  public static boolean getXO (String str) {
    int countX = 0;
    int countY = 0;
    for(int i=0;i<str.length();i++){
      if(str.charAt(i)=='X' || str.charAt(i)=='x')
        countX++;
      if(str.charAt(i)=='O' || str.charAt(i)=='o')
        countY++;
    }
    return countX == countY;
  }
}
```
