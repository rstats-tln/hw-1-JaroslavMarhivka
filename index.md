Homework 1: ggplot2
================
Your Name
2019-03-04

``` r
library(ggplot2)
```

By using *mpg* dataset:

1.  Map a continuous variable to color, size, and shape. How do these aesthetics behave differently for categorical vs. continuous variables?

-   Color

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = hwy, y = model, color = displ))
```

![](index_files/figure-markdown_github/unnamed-chunk-2-1.png)

-   Size

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = hwy, y = model, size = displ))
```

![](index_files/figure-markdown_github/unnamed-chunk-3-1.png)

-   Shape

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = hwy, y = model, shape = trans))+
  scale_shape_manual(values = 1:10)
```

![](index_files/figure-markdown_github/unnamed-chunk-4-1.png)

1.  What happens if you map the same variable to multiple aesthetics?

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = hwy, y = model, color = displ, size = displ))
```

![](index_files/figure-markdown_github/unnamed-chunk-5-1.png)

1.  What does the stroke aesthetic do? What shapes does it work with? (Hint: use ?geom\_point)

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = hwy, y = model, stroke = displ))
```

![](index_files/figure-markdown_github/unnamed-chunk-6-1.png)

1.  What happens if you map an aesthetic to something other than a variable name, like aes(colour = displ &lt; 5)?

``` r
ggplot(data = mpg) +
  geom_point(mapping = aes(x = hwy, y = model, color = displ < 5))
```

![](index_files/figure-markdown_github/unnamed-chunk-7-1.png)
