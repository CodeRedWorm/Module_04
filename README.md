# Module_04

Entered vectors into RStudio. Divided BP values by 100 so they would appear more easily on boxplot.
Columns <- c("Freq","BP","First","Second","FinalDecision")
Freq <- c(0.6,0.3,0.4,0.4,0.2,0.6,0.3,0.4,0.9,0.2)
BP <- c(1.03,0.87,0.32,0.42,0.59,1.09,0.78,2.05,1.35,1.76)
First <- c(1,1,1,1,0,0,0,0,NA,1)
Second <- c(0,0,1,1,0,0,1,1,1,1)
FinalDecision <- c(0,1,0,1,0,1,0,1,1,1)

Created a data frame (Blood) using the data from Freq and BP. Remove any NA value.
Blood <- data.frame(Columns,Freq,BP,First,Second,FinalDecision,stringsAsFactors=FALSE,na.rm=TRUE)

boxplot(Freq,BP,
main = "Multiple boxplots for blood test",
at = c(1,2),
names = c("Freq","BP (/100"),
col = c("red","yellow"),
horizontal = TRUE
)

hist(First, breaks=2, xaxt="n")
axis(1,at=seq(0,1,by=1),labels=c("Good","Bad"))

hist(Second, breaks=2, xaxt="n")
axis(1,at=seq(0,1,by=1),labels=c("Low","High"))

hist(FinalDecision, breaks=2, xaxt="n")
axis(1,at=seq(0,1,by=1),labels=c("Low","High"))

Boxplot
Median BP is close to 100, with the max being above 200 and the min being around 50 based on appearances.

Median frequency of visits in the last 12 months is around 0.4, with the min being close to 0.1 and max being around 0.8 based on appearances.

Histogram
First saw slightly more Bad assessments, although there was one result that was omitted.

Second saw more High or Bad assessments than the first doctor, although this one actually included results for all patients.

FinalDecision histogram matched that of the Second doctor, however four of the ten decisions differed between the two.
