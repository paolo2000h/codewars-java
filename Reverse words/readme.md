##Description:
Complete the function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.
##Examples:
```java
"This is an example!" ==> "sihT si na !elpmaxe"
"double  spaces"      ==> "elbuod  secaps"
```
##Solution:
```java
public class Kata
{
  public static String reverseWords(final String original)
  {
    String splited[] = original.split(" ");
    String reversed="";
    for(String a: splited){
      for(int i=a.length()-1;i>=0;i--){
        reversed+=a.charAt(i);
      }
      reversed+=" ";
    }
    if(reversed.length()==0){
      return original;
    }
    return reversed.substring(0,reversed.length()-1);
  }
}
```
