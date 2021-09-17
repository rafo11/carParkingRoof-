import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[][] arr = {
                {5, 4, 4},
                {4, 3, 4},
                {3, 2, 4},
                {2, 2, 2},
                {3, 3, 4},
                {1, 4, 4},
                {4, 1, 1},
        };
        System.out.println(number(arr));
    }


    public static void Solution(int[][] arr, int[][] clone, int k, int z, int m, int n) {
        if (clone[k][z] == -1) {
            return;
        }
        clone[k][z] = -1;
        if (k + 1 < m) {
            if (arr[k + 1][z] == arr[k][z]) {
                Solution(arr, clone, k + 1, z, m, n);
            }
        }
        if (k - 1 >= 0) {
            if (arr[k - 1][z] == arr[k][z]) {
                Solution(arr, clone, k - 1, z, m, n);
            }
        }
        if (z + 1 < n) {
            if (arr[k][z + 1] == arr[k][z]) {
                Solution(arr, clone, k, z + 1, m, n);
            }
        }
        if (z - 1 >= 0) {
            if (arr[k][z - 1] == arr[k][z]) {
                Solution(arr, clone, k, z - 1, m, n);
            }
        }
    }

    public static int number(int[][] arr) {
        int count = 0;
        int m = arr.length;
        int n = arr[0].length;
        if (m == 0 || n == 0) {
            return 0;
        }
        int[][] clone = Arrays.stream(arr).map(int[]::clone).toArray($ -> arr.clone());
        for (int k = 0; k < m; k++) {
            for (int z = 0; z < n; z++) {
                if (clone[k][z] >= 0) {
                    Solution(arr, clone, k, z, m, n);
                    count+=1;
                }

            }
        }
        return count;
    }
}
