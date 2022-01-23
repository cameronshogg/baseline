inv <- read.csv("Investigation-1.csv", header=T)
random <- read.csv("Random.csv", header=T)
consec <- read.csv("Consecutive.csv", header=T)

random$dayshift <- c(rep(1, 24), rep(2, 24), rep(3, 24), rep(4, 24),
                     rep(5, 24), rep(6, 24), rep(7, 24), rep(8, 24),
                     rep(9, 24), rep(10, 24), rep(11, 24), rep(12, 24), 
                     rep(13, 24), rep(14, 24), rep(15, 24))

hist(random$y300, breaks=30, main = "Histogram of Camshaft Straightness (y300)",
     xlab = "Straightness", col = "skyblue")
abline(v = c(-10, 10), lty = "dashed", col = "red")


plot(random$part, random$y300, type="l", 
     main = "Time Series Plot of Camshaft Straightness",
     xlab = "Part Number", ylab = "Camshaft Straightness")

boxplot(random$y300~random$day, main = "Boxplot of Camshaft Straightness by Day",
        xlab = "Day", ylab = "Camshaft Straightness", col = "coral1")
boxplot(random$y300~random$shift, main = "Boxplot of Camshaft Straightness by Shift",
        xlab = "Shift", ylab = "Camshaft Straightness", col="orchid")
boxplot(random$y300~random$dayshift, 
        main = "Boxplot of Camshaft Straightness by Day and Shift",
        xlab = "Day and Shift", ylab = "Camshaft Straightness", col="aquamarine3")

range(random$y300)

summary(random$y300)
var(random$y300)
sd(random$y300)
mean(random$y300, trim=0.05)

sd(random$y300/sqrt(length(random$y300)))

library(gmodels)
ci(random$y300, confidence=0.95, alpha=1-0.95)
