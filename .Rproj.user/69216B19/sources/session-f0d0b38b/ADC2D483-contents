my_data <- read.csv("/Users/ivymbunda/Documents/GitHub/Predicting-Math-scores-using-Linear-Regression/StudentsPerformance.csv")

#Explore the structure of the dataset
str(my_data) 

#lets look at the first few rows of the data set
head(my_data)  

# lets generate a summary of the numerical variables
summary(my_data)  # Generate summary statistics for numerical variables

# Data visualization
 #Histogram of math scores
hist(my_data$math.score, 
     main = "Histogram of Math Scores", 
     xlab = "Math Score",
     ylab = "Frequency")

# Scatterplot of math scores vs. reading scores
plot(my_data$math.score, my_data$reading.score, 
     main = "Scatterplot of Math Scores vs. Reading Scores", 
     xlab = "Math Score", 
     ylab = "Reading Score")

# Calculate correlation between math and reading scores
cor(my_data$math.score, my_data$reading.score)

#Compare mean math scores between male and female students
t.test(math.score ~ gender, data = my_data)

# Compare mean math scores between different types of lunch
t.test(math.score ~ lunch, data = my_data)

# Create a linear regression model to predict math scores based on other variables
lm_model <- lm(math.score ~ reading.score + writing.score + gender + lunch, data = my_data)
summary(lm_model)  # View summary of the linear regression model

