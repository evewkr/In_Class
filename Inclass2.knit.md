---
title: "In class Exercise 7 - Visualising and Analysing Geographic Data"
---





::: {.cell}

```{.r .cell-code}
p2 <- ggplot(data=exam_data, 
             aes(x = ENGLISH)) +
  geom_histogram(bins=20, 
                 boundary = 100,
                 color="grey25", 
                 fill="grey90") +
  coord_cartesian(xlim=c(0,100)) +
  ggtitle("Distribution of English scores")
```
:::

::: {.cell}

```{.r .cell-code}
p3 <- ggplot(data=exam_data, 
             aes(x= MATHS, 
                 y=ENGLISH)) +
  geom_point() +
  geom_smooth(method=lm, 
              size=0.5) +  
  coord_cartesian(xlim=c(0,100),
                  ylim=c(0,100)) +
  ggtitle("English scores versus Maths scores for Primary 3")
```

::: {.cell-output .cell-output-stderr}
```
Warning: Using `size` aesthetic for lines was deprecated in ggplot2 3.4.0.
ℹ Please use `linewidth` instead.
```
:::
:::

