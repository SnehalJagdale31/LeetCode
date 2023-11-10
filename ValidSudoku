class Solution {
    public boolean isValidSudoku(char[][] board) {
        Set<Character>[] rowSet = new HashSet[9];
        Set<Character>[] colSet = new HashSet[9];
        Set<Character>[] gridSet = new HashSet[9];
        
        for(int i = 0; i < 9; i++) {
            rowSet[i] = new HashSet<>();
            colSet[i] = new HashSet<>();
            gridSet[i] = new HashSet<>();
        }
        
        for(int i = 0; i < 9; i++) {
            for(int j = 0; j < 9; j++) {
                char value = board[i][j];
                if (value == '.') {
                    continue;
                }
                
                int gridNo = (i/3) * 3 + j/3;
                boolean isPresentInRow = rowSet[i].contains(value);
                
                boolean isPresentInCol = colSet[j].contains(value);
                
                boolean isPresentInGrid = gridSet[gridNo].contains(value);
                
                if (isPresentInRow || isPresentInCol || isPresentInGrid) {
                    return false;
                }
                
                rowSet[i].add(value);
                colSet[j].add(value);
                gridSet[gridNo].add(value);
            }
        }
        
        return true;
    }
}
