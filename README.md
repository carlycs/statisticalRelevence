please also update the text
- add median
the t-test
and generell the other improvements you did except the first both comments

For future work, more data collection and randomization for the experiment set up is suggested. For example, for the data collected for gender we have 
a simple box plot comparison and visuallized the results using box plot. This type of work would better show how gender in particular would affect this 
market.

b1 <- c(5,	7,	15,	11,	4)
b2 <- c(2	,5,	13,	14,	8)
b3 <- c(1,	6,11,	14,10)
b4 <- c(1,	4	,1	,15,	21)
lengval <- sum(b1)


starVar <-vector(mode='integer', length = lengval)
finalList <- NULL
dd <-1 
for (i in 1:5){
  starVar[dd:a[i]] <- rep(i, a[i])
  dd=a[i]
 
}

###
bb <- read.csv("/home/hoof/Desktop/statisticalrelevence/data_research_csv.csv", head=TRUE)
databb <- data.frame(bb)

boxplot(Rate.Confidence ~ Gender, data=databb,
        main="Gender Study over effect of Confidence on Virtual Teams Success", 
        xlab="Gender", ylab="Rated Confidence from 0 to 1")

h <- hist(databb$rate.the.influence.of.incentives, col=blues9,
          xlab="Influece of Insentive Rated", 
          main="Histogram with Normal Curve")
x <- databb$rate.the.influence.of.incentives
xfit<-seq(min(x),max(x),length=40) 
yfit<-dnorm(xfit,mean=mean(x),sd=sd(x)) 
yfit <- yfit*diff(h$mids[1:2])*length(x) 
lines(xfit, yfit, col="blue", lwd=2)
