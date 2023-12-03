# Lab Report 5
## EdStem thread: reverse vowels assigment:
### The goal of this assignment is to write a fucntion that takes a string, and reverses the order of all the vowels in there (e.g hello -> holle).

<br>

#### EdStem thread: Error when testing the reverse vowels method!
![Image](bash.png)
<br>
<br>
Below you can find my code for the reverse vowels method as well as the code for my testing method respectively.
<br>
```java
void swap(char[] chars, int x, int y) {
        char temp = chars[x];
        chars[x] = chars[y];
        chars[y] = temp;
    }
    
    public String reverseVowels(String s) {
        int start = 0;
        int end = s.length() - 1;

        char[] sChar = s.toCharArray();
        
        while (start < end) {
            
            while (start < s.length () && isVowel(sChar[start])) {
                start++;
            }

            while (end >= 0 && isVowel(sChar[end])) {
                end--;
            }

            if (start < end) {
                swap(sChar, start++, end--);
            }
        }
        

        return new String(sChar);
    }
```

```java
public void testReverseVowels1() {
        Solution solution = new Solution();
        String input = "Hello World!";
        String expected = "Hollo Werld!";
        assertEquals(expected, solution.reverseVowels(input));
    }
```
I wrote a test case that takes the string "Hello World!" and is supposed to return "Hollo Werld!". However, my function returns a string that looks nothing like this at all. My guess is that I am swapping the characters at the wrong time and I made a mistake in some part of my logic, however, I can not figure out what part. I also looked at my `isVowel` method and I believe it looks correct. <br>
Can i please get some help on what could be possibly going wrong? 
Thank you!

#### EdStem TA respone: Re- Error when testing the reverse vowels method!
Dear student, I was able to take a look at your `testReverseVowels1` method and it looks correct so that eliminates one source for the problem. The `isVowels` method is also correct as it checks for every lower and upper case vowel. This narrows down the problem to the logic of the `reverseVowels` function. My hint to you is to look within the reverseVowels method, and carefully observe the conditions in the inner while loops where vowel checking takes place. Consider the role of these conditions in determining when to move the start and end pointers. Pay attention to how the loop logic should respond to vowels and non-vowels. In other words, when do we move the right pointer and when do we right the left pointer with respect to a `Char` being a vowel or not being a vowel. <br>
Lastly, I wanted you to notice how I went about potentially finding the bug in the code. A method that always helps is to eliminate different factors that could potentially be casuing problems, narrowing down the source of the problem. <br>
Let me know if that helps!
