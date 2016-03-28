# sparr R Package Notes

[*sparr* (spatial relative risk) R package](https://cran.r-project.org/web/packages/sparr/index.html) was developed to perform both fixed bandwidth kernel density estimation (KDE) and adaptive bandwidth KDE. The online documentation is [here](https://cran.r-project.org/web/packages/sparr/sparr.pdf). There some changes to the preset dataset *primary biliary cirrhosis* (**PBC**) in *sparr*. Here are some code updates for section 4 (Code examples): 

**Reconstruct the nested list**

    data("PBC")
    data<- cbind(PBC$x, PBC$y)
    ID<- PBC[["marks"]]
    data<- data.frame(cbind(data, ID))
    data[data$ID==2,]$ID<- 0

After regenerate PBC data, the code should be OK to run. 

