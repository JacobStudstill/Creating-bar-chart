# Creating-bar-chart

# Jacob Studstill | LIS4370 | Module 3 Assignment
install.packages("tidyverse")
library(ggplot2)

Name <- c("Jeb", "Donald", "Ted", "Marco", "Carly", "Hillary", "Bernie")
ABC_poll   <- c(  4,      62,      51,    21,      2,        14,       15)
CBS_poll   <- c( 12,      75,      43,    19,      1,        21,       19)

df_polls <- data.frame(Name, ABC_poll, CBS_poll)
# Using str to inspect data
str(df_polls)
# Using head to inspect data
head(df_polls)

# Find the mean of both polls
mean(df_polls$ABC_poll)
mean(df_polls$CBS_poll)

# Find the median of both polls
median(df_polls$ABC_poll)
median(df_polls$CBS_poll)

# Find range of both polls
range(df_polls[, c("ABC_poll","CBS_poll")])

# Column with difference for polls
df_polls$Diff <- df_polls$CBS_poll - df_polls$ABC_pol
df_polls$Diff

ggplot(df_polls, aes(x = Name, y = Diff, fill= Name)) +
  geom_col()

  <img width="679" height="550" alt="programPlot" src="https://github.com/user-attachments/assets/dcbe2b9a-d5d9-412b-b48f-6ed2e2f82821" />
