# day24

## 下面这段代码输出什么

```golang
func main() {
    m := map[int]string{0: "zero", 1: "one"}
    for k, v := range m {
        fmt.Println(k, v)
    }
}
```

## 下面这段代码输出什么呢

```golang
func main() {
    a := 1
    b := 2
    defer calc("1", a, calc("10", a, b))

    a = 0
    defer calc("2", a, calc("20", a, b))
    b = 1
}

func calc(index string, a, b int) int {
    ret := a + b
    fmt.Println(index, a, b, ret)
    return ret
}
```
