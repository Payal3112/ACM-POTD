//backspace-string-compare

class Solution {

    public String build(String s) {
        String result = "";

        for(int i = 0; i < s.length(); i++) {

            char ch = s.charAt(i);

            if(ch == '#') {
                if(result.length() > 0) {
                    result = result.substring(0, result.length() - 1);
                }
            } 
            else {
                result = result + ch;
            }

        }

        return result;
    }

    public boolean backspaceCompare(String s, String t) {

        String a = build(s);
        String b = build(t);

        return a.equals(b);
    }
}

<img width="1915" height="871" alt="image" src="https://github.com/user-attachments/assets/fab0624d-0cbf-4b06-9ec2-f2d83292038c" />

