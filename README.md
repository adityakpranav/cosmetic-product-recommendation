# Cosmetic-product-recommendation

A cosmetic product company wants to reward its loyal customers by giving them a heavy discount on the products they buy repeatedly. Probability of buying these products on the next visit is computed using a heuristic. Higher probability scores meant higher relevancy. Based on the scores the company wants to allocate the most relevant set of products to customers.


## Objective:

The objective of the hackathon is to allocate the most relevant set of products to each customer by maximizing total relevancy. You should use the column “relevancy_score” of Relevancy_table to get relevancy of products for customers.

## Constraints:

1. Due to budget constraints, there is fixed volume of each product. For instance, product “5650512” cannot be allocated to more than 150 customers. Use the “Volume” column of the Products table.

2. A customer can get maximum 8 products and minimum 3 products. Drop all the customers who qualify for less than 3 products. 

3. There are some set of products which cannot be assigned together (e.g. product “5649565” and “5649646” cannot be given together to any customer). You can get this list in the Exclusion table.

4. All the products allocated to a customer should be distinct (i.e. the same product cannot be allocated twice to the same customer)

## Data Table:

1. Relevency_table : Customers relevancy score for eligible products

ID | Value | Sample
--- | --- | ---  
customers | object | A10001
product | int64 | 5649565
relevancy_score | float64 | 0.293978166

2. Products : products on offer and their max volume limit

ID | Value | Sample
--- | --- | ---  
product | int64 | 5649565
volume | int64 | 200

3. Exclusion : Mutually exclusive products, which cannot be allocated to same customer together

ID | Value | Sample
--- | --- | ---  
product1 | int64 | 5649565
product2 | int64 | 5749560

## Output Expected:

The output file should complete the objective of the hackathon and should be in the format as Sample submissions.

Sample Submission (Download)

### Deliverables:

    Output file

    Source code (Submit your Code in Python only)


### Judging Criteria:

    Number of constraints satisfied

    Total relevancy captured (i.e sum of relevancy_score column of output file)
