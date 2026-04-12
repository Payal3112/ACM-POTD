//Flood Fill
class Solution {

    public int[][] floodFill(int[][] image, int sr, int sc, int color) {

        int original = image[sr][sc];

        if(original == color) return image;

        dfs(image, sr, sc, original, color);

        return image;
    }

    public void dfs(int[][] image, int r, int c, int original, int color){

        if(r < 0 || c < 0 || r >= image.length || c >= image[0].length)
            return;

        if(image[r][c] != original)
            return;

        image[r][c] = color;

        dfs(image, r+1, c, original, color);
        dfs(image, r-1, c, original, color);
        dfs(image, r, c+1, original, color);
        dfs(image, r, c-1, original, color);
    }
}

<img width="1918" height="927" alt="image" src="https://github.com/user-attachments/assets/9cedb082-0dc0-42f6-8dde-7629f2541d1f" />
