# Lattice Plotting System



```r
#Simple Lattice plot 1
library(datasets)
library(lattice)

##Simple scatter plot
xyplot(Ozone ~ Wind, data = airquality)
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-11.png) 

```r
#Simple Lattice plot 2
library(datasets)
library(lattice)

## Convert 'Month' to a factor variable
airquality <- transform(airquality, Month = factor(Month))
xyplot(Ozone ~ Wind | Month, data = airquality, layout = c(5, 1))
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-12.png) 

```r
## The system works by returning a graphic object Trellis and then printing it using the lattice functions
## for printing
p <- xyplot(Ozone ~ Wind, data = airquality)  ## Nothing happens!
print(p)  ## Plot appears
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-13.png) 

