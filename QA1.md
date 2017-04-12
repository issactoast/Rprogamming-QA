# QA.1
Issac Lee  
`r format(Sys.Date())`  



## Question
안녕하세요. rbind() 혹은 bind_rows()를 사용하는 방법과 관련하여 질문드립니다.

X 라는 임의의 데이터 프레임이 있을 때, X를 N번 생성하여 그것들을 행으로 합쳐 새로운 데이터 프레임 Y를 만드는 간편한 방법이 있는지 여쭈어보고 싶네요.



```r
library(dplyr)
N<-1000
Y<-data.frame()
for (j in 1:N) {
  Y<-bind_rows(Y, X)
}
```

와 같이 코드를 작성하였는데, 혹시나 이와 같이 for 문을 사용하지 않고 해당 내용을 수행할 수 있는지 여쭈어 보고 싶습니다.  

## Answer
dplyr, purrr 팩키지를 이용하자. map_df() 함수의 경우는 결과값이 다시 데이터 프레임으로 반환된다.


```r
library(dplyr)
library(purrr)
 
x <- matrix(c(1:100), nrow = 5)
x <- as.data.frame.array(x)
Y <- data.frame()
N <- 100
 
f <- function(foo){ bind_rows(Y,x)}
Y <- map_df(1:N, f)
```

