//Pascal Triangle

import java.util.*;

class Solution {
    public List<List<Integer>> generate(int numRows) {
        List<List<Integer>> ans = new ArrayList<>();

        for (int i = 0; i < numRows; i++) {
            List<Integer> row = new ArrayList<>();

            for (int j = 0; j <= i; j++) {
                // first and last element
                if (j == 0 || j == i) {
                    row.add(1);
                } else {
                    List<Integer> prev = ans.get(i - 1);
                    row.add(prev.get(j - 1) + prev.get(j));
                }
            }

            ans.add(row);
        }

        return ans;
    }
}

<img width="1910" height="880" alt="image" src="https://github.com/user-attachments/assets/38fb0d98-a674-46e6-82be-e2b29449ff8c" />
