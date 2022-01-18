# 搜索二维矩阵 II
难度：中等

## 描述
编写一个高效的算法来搜索 m x n 矩阵 matrix 中的一个目标值 target 。该矩阵具有以下特性：

每行的元素从左到右升序排列。
每列的元素从上到下升序排列。

![image](https://user-images.githubusercontent.com/45349601/149908931-04cf4ecf-6d1c-4006-9a43-e511f8c0ebec.png)

![image](https://user-images.githubusercontent.com/45349601/149908738-8d5ceca2-6832-4afd-af02-6f016b78adc3.png)

## 代码
```java
class Solution {
    public boolean searchMatrix(int[][] matrix, int target) {
        int m = matrix.length, n = matrix[0].length;
        int x = 0, y = n - 1;
        while (x < m && y >= 0) {
            if (matrix[x][y] == target) {
                return true;
            }
            if (matrix[x][y] > target) {
                --y;
            } else {
                ++x;
            }
        }
        return false;
    }
}
```

## 备注
![image](https://user-images.githubusercontent.com/45349601/149909040-3838c7c1-dfb7-40b8-8ed6-3c6f203fee40.png)
![image](https://user-images.githubusercontent.com/45349601/149909088-33be804b-c0b4-4dc5-b67d-044698929d59.png)
