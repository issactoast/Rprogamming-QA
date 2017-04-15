# QA.3
Issac Lee  
`r format(Sys.Date())`  



## [QA.3](https://www.facebook.com/groups/krstudy/permalink/758124034361871/)

안녕하세요!
제가 이러한 행렬을 outer함수를 이용해서 만드려는데 어떻게 만들어야할까요...?
for문을 사용해서는 금방 만들었는데 outer 함수를 써서 만들라니 감이 전혀 안오네요... ㅠㅠ
일반적인 n*n matrix에서도 동일하게 나와야합니다..!

![*원하는 행렬모양](https://scontent-ord1-1.xx.fbcdn.net/v/t1.0-9/17457280_1230268010427724_2598839797147084228_n.jpg?oh=19f0090103ee62130b0ec14710cb3deb&oe=59965406)

## Answer
R의 [outer()](https://stat.ethz.ch/R-manual/R-devel/library/base/html/outer.html)은 수학 외적의 일반화 버젼이라고 생각할 수 있다. 이 함수를 잘 사용하면 시간이 많이 드는 loop문들을 사용하지 않고 계산을 할 수 있는 장점이 있다.


```r
g <- function(x, y){
pmax((2 - abs(x - y)), 0)
}

my.matrix <- function(n, f){
  x <- 1:n
  y <- n:1
  outer(x, y, f)
}

my.matrix(5, g)
```

```
##      [,1] [,2] [,3] [,4] [,5]
## [1,]    0    0    0    1    2
## [2,]    0    0    1    2    1
## [3,]    0    1    2    1    0
## [4,]    1    2    1    0    0
## [5,]    2    1    0    0    0
```
