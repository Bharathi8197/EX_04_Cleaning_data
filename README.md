Exp 4 : Explore Various Variable and Row Filters in R for Cleaning Data & Apply Plot Features on Sample Datasets

AIM:
To explore and apply various row and column (variable) filters in R for cleaning data and visualize the results using different plotting functions.

EQUIPMENTS REQUIRED:
R Language (via RStudio or CLI)
Dataset: Iris dataset (URL)

ALGORITHM:
Load the dataset from a URL using read.csv().
Explore the structure and summary of the dataset.
Apply filters to rows and columns for cleaning/subsetting.
Visualize data using boxplots, histograms, and scatter plots.

Program:

# Step 1: Load dataset from URL
url <- "https://raw.githubusercontent.com/uiuc-cse/data-fa14/gh-pages/data/iris.csv"
iris_data <- read.csv(url)

# Step 2: View structure and summary
print("Structure of dataset:")
str(iris_data)

print("Summary of dataset:")
summary(iris_data)

# Step 3: Filter rows where Sepal.Length > 5
filtered_data <- iris_data[iris_data$Sepal.Length > 5, ]
print("Filtered rows (Sepal.Length > 5):")
head(filtered_data)

# Step 4: Select only Sepal.Length and Petal.Length columns
selected_columns <- iris_data[, c("Sepal.Length", "Petal.Length")]
print("Selected columns:")
head(selected_columns)

# Step 5: Boxplot of Sepal.Width
boxplot(iris_data$Sepal.Width,
        main = "Boxplot of Sepal Width",
        ylab = "Sepal Width",
        col = "lightblue")

# Step 6: Histogram of Petal.Length
hist(iris_data$Petal.Length,
     main = "Histogram of Petal Length",
     xlab = "Petal Length",
     col = "lightgreen",
     breaks = 15)

# Step 7: Scatterplot of Sepal.Length vs Petal.Length
plot(iris_data$Sepal.Length, iris_data$Petal.Length,
     main = "Sepal vs Petal Length",
     xlab = "Sepal Length",
     ylab = "Petal Length",
     col = iris_data$Species,
     pch = 19)


EXPECTED OUTPUT:
The structure and summary of the dataset will be displayed in the console.
Filtered records with Sepal Length > 5.
Selected columns (Sepal Length and Petal Length).
Visualizations:
A boxplot for Sepal Width.
A histogram for Petal Length.
A scatter plot showing Sepal vs Petal Length with points colored by species.

RESULT:
Successfully filtered and visualized data loaded directly from a URL in R using built-in functions.
