# EECS731Project5
Worldwide Product Prediction


# Data Info

The dataset contains historical product demand for a manufacturing company with footprints globally. The company provides thousands of products within dozens of product categories. There are four central warehouses to ship products within the region it is responsible for. 

It contains five columns: 
Product_CodeThe product name encoded

WarehouseWarehouse name encoded

Product_CategoryProduct Category for each Product_Code encoded

DateThe date customer needs the product

Order_Demandsingle order qty


# Part 1: Data Exploration

We clean the data by removing the null values and transform the object-type Order_Demand into numerical quantities for better leverage. 

We find how many kinds of product in each category and the demand number for each category.  The results show that category_019 contains most kinds of product and the demand is also the highest within this category. 




# Part 2: Forecasting 

Based on part 1, we choose the category_019 as our object for learning and prediction. We change the dataframe into a time series and adopt the Prophet model to do this task. 

Before learning, we use Box-Cox data transformations to evaluate a set of lambda coefficients (λ) and selects the value that achieves the best approximation of normality. It results a pretty good prediction for the number of demands in the future. 










#Conclusion

Since the products are manufactured in different locations all over the world, it normally takes more than one month to ship products via ocean to different central warehouses. If forecasts for each product in different central with reasonable accuracy for the monthly demand for month after next can be achieved, it would be beneficial to the company in multiple ways.
