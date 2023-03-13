# leftroty
class Solution {
  public:
    vector<vector<int>> rotateMatrix(int N, int M, int K,
                                     vector<vector<int>> Mat) {
        // code here
      vector<vector<int>>result(N,vector<int>(M));
      for(int i=0;i<N;i++){
          for(int j=0;j<M;j++){
              int x=(j+K)%M;
              result[i][j]=Mat[i][x];
          }
      }
      return result;
    }
};
