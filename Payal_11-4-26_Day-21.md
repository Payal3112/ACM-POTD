//make-the-string-great

import java.util.Stack;

class Solution {
    public String makeGood(String s) {
Stack<Character> stack = new Stack<>();
        for(int i = 0; i < s.length(); i++) {
            char c= s.charAt(i);

            if(!stack.isEmpty() && Math.abs(stack.peek() - c) == 32) {
                stack.pop();  
            }
            else {
                stack.push(c); // add character
            }
        }

        String result = "";

        for(char ch : stack) {
            result += ch;
        }

        return result;
    }
}

<img width="1918" height="866" alt="image" src="https://github.com/user-attachments/assets/192015ee-d8b8-40b0-94bc-f9f781ae3390" />
