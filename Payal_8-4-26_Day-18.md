//Remove All Adjacent Duplicates In String

class Solution {

    public String removeDuplicates(String s) {

        StringBuilder stack = new StringBuilder();

        for(char ch : s.toCharArray()){

            int len = stack.length();

            if(len > 0 && stack.charAt(len - 1) == ch){
            
                stack.deleteCharAt(len - 1); // remove duplicate
            }
            else{
            
                stack.append(ch); // push
            }
        }

        return stack.toString();
    }
}

<img width="1902" height="838" alt="image" src="https://github.com/user-attachments/assets/32a8fb63-9460-40fa-b0aa-42c046690fea" />
