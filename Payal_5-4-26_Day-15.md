//Vlaid parenthesis

class Solution {
    
    public boolean isValid(String s) {
        Stack<Character> stack = new Stack<>();
        for (char c : s.toCharArray()) {
            if (c == '(' || c == '{' || c == '[') {
                stack.push(c);
            } else {
                if (stack.isEmpty()) return false;
                char top = stack.pop();
                if ((c == ')' && top != '(') || 
                    (c == '}' && top != '{') || 
                    (c == ']' && top != '[')) {
                    return false;
                }
            }
        }
        return stack.isEmpty();
    }
}
        
<img width="1903" height="852" alt="image" src="https://github.com/user-attachments/assets/788defa6-62a1-4ec9-acfc-cb5dd89ca8d8" />

