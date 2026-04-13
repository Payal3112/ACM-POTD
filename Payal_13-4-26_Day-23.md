//FIND JUDGE

class Solution {
    public int findJudge(int n, int[][] trust) {

        boolean[] trustsSomeone = new boolean[n + 1];

        // Step 1: mark people who trust someone
        for (int[] t : trust) {
            int a = t[0];
            trustsSomeone[a] = true;
        }

        // Step 2: find candidate who trusts nobody
        for (int i = 1; i <= n; i++) {

            if (!trustsSomeone[i]) { // candidate judge

                int count = 0;

                // check how many trust this person
                for (int[] t : trust) {
                    if (t[1] == i) {
                        count++;
                    }
                }

                if (count == n - 1) {
                    return i;
                }
            }
        }

        return -1;
    }
}

<img width="1917" height="862" alt="image" src="https://github.com/user-attachments/assets/2ed1c800-3808-4fc6-95ad-de522bb50d72" />
