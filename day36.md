# day36

## 关于函数声明，下面语法正确的是

```text
A. func f(a, b int) (value int, err error)
B. func f(a int, b int) (value int, err error)
C. func f(a, b int) (value int, error)
D. func f(a int, b int) (int, int, error)
```

## 关于整型切片的初始化，下面正确的是

```text
A. s := make([]int)
B. s := make([]int, 0)
C. s := make([]int, 5, 10)
D. s := []int{1, 2, 3, 4, 5}
```

## 下面代码会触发异常吗？请说明

```golang
func main() {
    runtime.GOMAXPROCS(1)
    int_chan := make(chan int, 1)
    string_chan := make(chan string, 1)
    int_chan <- 1
    string_chan <- "hello"
        select {
        case value := <-int_chan:
            fmt.Println(value)
        case value := <-string_chan:
            panic(value)
     }
}
```
