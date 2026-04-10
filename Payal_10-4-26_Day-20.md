//Remove outermost paranthesis

class Solution {

    public String removeOuterParentheses(String String) {

        int n=String.length();

        int count=0;

        String ans="";

        for (int i=0;i<n;i++){

            char c= String.charAt(i);

            if(c ==')'){

                count--;

            }
            if (count!=0){

                ans+=c;

            }
            if(c == '('){

                count++;
            }
        }return ans;
}
}

<img width="1900" height="867" alt="image" src="https://github.com/user-attachments/assets/5c6db25c-4a0f-47c8-9efb-a9194a8e6a8a" />


