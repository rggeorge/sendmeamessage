library(tidyr)
library(dplyr)

heart <- read.csv("titanic_original.csv", header = TRUE, stringsAsFactors = FALSE)

heart$embarked[which(is.na(heart$embarked))] <- "S"
heart$age[which(is.na(heart$age))] <- mean(heart$age, na.rm = TRUE)
heart$boat[which(is.na(heart$boat))] <- "NA"
heart$cabin[which(is.na(heart$cabin))] <- "NA"
heart$has_cabin_number <- ifelse(is.na(heart$cabin), 0, 1)

write.csv(heart, file = "titanic_clean.csv")
