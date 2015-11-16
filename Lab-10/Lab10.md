## Lab 10 Blog
---------------------------------------

#### Group Members: 
  * Aaron Cheng
  * Haoxin Luo

---------------------------------------

##### Part 1
1. First we got 
2. I read Chapter 9 of the book on [Association Rule Mining](https://cran.r-project.org/doc/contrib/Zhao_R_and_data_mining.pdf) and followed the tutorial. Here is my code:
    ```r
    str(titanic.raw)
    df <- as.data.frame(titanic.raw)
    head(df)
    titanic.raw <- NULL
    for(i in 1:4) {
      titanic.raw <- cbind(titanic.raw, rep(as.character(df[,i]), df$Freq) )
    }
    titanic.raw <- as.data.frame(titanic.raw)
    names(titanic.raw) <- names(df)[1:4]
    dim(titanic.raw)
    str(titanic.raw)
    head(titanic.raw)
    summary(titanic.raw)
    
    library(arules)
    rules.all <- apriori(titanic.raw)
    rules.all
    inspect(rules.all)
    
    rules <- apriori(titanic.raw, control = list(verbose=F),
                     parameter = list(minlen=2, supp=0.005, conf=0.8),
                     appearance = list(rhs=c("Survived=No", "Survived=Yes"),
                                       default="lhs"))
    quality(rules) <- round(quality(rules), digits=3)
    rules.sorted <- sort(rules, by="lift")
    inspect(rules.sorted)
    
    rules <- apriori(titanic.raw, control = list(verbose=F),
                     parameter = list(minlen=3, supp=0.002, conf=0.2),
                     appearance = list(rhs=c("Survived=Yes"),
                                       lhs=c("Class=1st", "Class=2nd", "Class=3rd", "Age=Child", "Age=Adult"), 
                                       default="none"))
    #quality(rules) <- round(quality(rules), digits=3)
    rules.sorted <- sort(rules, by="confidence" )
    inspect(rules.sorted)
    
    rules <- apriori(titanic.raw, control = list(verbose=F),
                     parameter = list(minlen=3, supp=0.002, conf=0.2),
                     appearance = list(rhs=c("Survived=Yes"),
                                       lhs=c("Class=1st", "Class=2nd", "Class=3rd", "Age=Child"), 
                                       default="none"))
    quality(rules) <- round(quality(rules), digits=3)
    rules.sorted <- sort(rules, by="confidence" )
    inspect(rules.sorted)
    
    source("http://bioconductor.org/biocLite.R")
    biocLite("Rgraphviz")
    
    library(arulesViz)
    plot(rules.all)
    plot(rules.all, method="grouped")
    plot(rules.all, method="graph")
    plot(rules.all, method="graph", control=list(type="items"))
    plot(rules.all, method="paracoord", control=list(reorder=TRUE))
    ```
3. Then, I played around with some of the parameters of the rules:
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_6.png)
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_7.png)
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_8.png)

4. Finally, I plotted the rules using different types of graphs:
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_1.png)
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_2.png)
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_3.png)
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_4.png)
    ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab9_5.png)
