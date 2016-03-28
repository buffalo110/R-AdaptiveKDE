# sparr R Package Notes

*sparr* (spatial relative risk) R package was developed to perform both fixed bandwidth kernel density estimation (KDE) and adaptive 
bandwidth KDE. The online documentation is [here](https://cran.r-project.org/web/packages/sparr/sparr.pdf). There some changes to the 
preset dataset primary biliary cirrhosis (PBC) in *sparr*. Here are some code updates for section 4, Code examples: 

**To produce Figure 1**

    data("PBC")
    par(mfrow = c(1,2))
    plot(PBC$window, main="cases")
    axis(1)
    axis(2)
    title(xlab = "Easting", ylab = "Northing")
    PBC$data<- cbind(PBC$x, PBC$y)
    points(PBC$data[PBC$marks =="case", 1:2], cex=0.8)
    plot(PBC$window, main="controls")
    axis(1)
    axis(2)
    title(xlab = "Easting", ylab = "Northing")
    points(PBC$data[PBC$marks =="control", 1:2], pch=3, cex=0.8)
    par(mfrow = c(1,1))

