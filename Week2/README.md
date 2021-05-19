# Week2
# ポインタ
今週は、ポインタについて学習していきます。
ポインタは関数・クラスを使用していく際に必ず必要になっていく概念です。
<p align="center"><a href="http://c-lang.sevendays-study.com/ex-day2.html">ポインタとアドレス</a></p>
<p align="center"><a href="http://c-lang.sevendays-study.com/ex-day3.html">ポインタと配列  </a></p>

## 一問目
配列a=[N]について、関数を用いて値を代入して下さい。
各要素の値は要素番号とします。

(ターミナル実行例)
```
a[1]=1
a[2]=2
   :
   :
   :
```
## 二問目
Week1で作成したソースコードを関数を利用して見やすくしてください。ユーザフレンドリーに。vector型を使いましょう。
####  １週目のソースコード
```
#include <stdlib.h>
#include <iostream>
#include <time.h>
#include <vector>
#define RAW_1 3
#define COLUMN_1 4
#define RAW_2 4//　COLLUMN_1 == RAW_2が成り立たなければならない
#define COLUMN_2 5

int main(void)
{
    std::vector<std::vector<int>> matrix_1;
    std::vector<std::vector<int>> matrix_2;
    std::vector<std::vector<int>> result_matrix;
    
    srand((unsigned int)time(NULL));

    std::cout << "行列１" << std::endl;
    for (int i = 0; i < RAW_1; i++) {//ここを関数化!!!
        std::vector<int> a1;
        for (int j = 0; j < COLUMN_1; j++) {
            int num_a1 = rand() % 10;
            a1.push_back(num_a1);
            std::cout << "a[" << i << "][" << j << "]:" << num_a1 << "      ";
        }
        std::cout << std::endl;
        matrix_1.push_back(a1);
    }

    std::cout << "行列２" << std::endl;
    for (int i = 0; i < RAW_2; i++) {//ここを関数化!!!
        std::vector<int> a2;
        for (int j = 0; j < COLUMN_2; j++) {
            int num_a2 = rand() % 10;
            a2.push_back(num_a2);
            std::cout << "b[" << i << "][" << j << "]:" << num_a2 << "      ";
        }
        std::cout << std::endl;
        matrix_2.push_back(a2);
    }

    for (int i = 0; i < RAW_1; i++) {
        std::vector<int> result;
        for (int j = 0; j < COLUMN_2; j++) {
            result.push_back(0);
        }
        result_matrix.push_back(result);
    }
    

    std::cout << "行列1 ×　行列2" << std::endl;
    for (int i = 0; i < RAW_1; i++) {//ここを関数化!!!
        for (int j = 0; j < COLUMN_2; j++) {
            for (int k = 0; k < RAW_2; k++) {
                result_matrix[i][j] += matrix_1[i][k] * matrix_2[k][j];
            }
            std::cout << "b[" << i << "][" << j << "]:" << result_matrix[i][j] << "      ";
        }
        std::cout << std::endl;
    }


}
```

## 三問目
二問目の実行結果をテキストファイルに出力して下さい。

(テキストファイル例)
```

作成した行列：[[[],[]],[[],[]]]

足し算結果：[[],[]]

掛け算結果：[[],[]]
```
<p align="left"><a href="https://github.com/ERiC-Labo/C_Journal_club/tree/main/Week1">Week1のリンク</a></p>
<p align="right"><a href="https://github.com/ERiC-Labo/C_Journal_club/tree/main/Week3">Week3のリンク</a></p> 
