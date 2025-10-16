# Amazon_ML_Challenge_2025
**TEAM_NAME** - Maverick_000

<img width="1918" height="610" alt="Screenshot 2025-10-15 002016" src="https://github.com/pradyumna-000/Amazon_ML_Challenge_2025/blob/main/Screenshot%202025-10-16%20183252.png?raw=true" />


## Problem Statement -
### Smart Product Pricing Challenge 
In e-commerce, determining the optimal price point for products is crucial for marketplace success 
and customer satisfaction. Your challenge is to develop an ML solution that analyzes product details 
and predict the price of the product. The relationship between product attributes and pricing is 
complex - with factors like brand, specifications, product quantity directly influence pricing. Your task 
is to build a model that can analyze these product details holistically and suggest an optimal price.

**Data Description**: 
The dataset consists of the following columns: 
1. sample_id: A unique identifier for the input sample 
2. catalog_content: Text field containing title, product description and an Item Pack Quantity(IPQ) 
concatenated. 
3. image_link: Public URL where the product image is available for download. Example link - 
https://m.media-amazon.com/images/I/71XfHPR36-L.jpg (https://m.media
amazon.com/images/I/71XfHPR36-L.jpg) To download images, use the download_images function 
from src/utils.py. See sample code in src/test.ipynb. 
4. price: Price of the product

**Evaluation Criteria**: 

Submissions are evaluated using Symmetric Mean Absolute Percentage Error (SMAPE):
A statistical 
measure that expresses the relative difference between predicted and actual values as a percentage, 
while treating positive and negative errors equally. <br>

Formula: 

SMAPE = (1/n) * Σ |predicted_price - actual_price| / ((|actual_price| + |predicted_price|)/2) <br>
Example: If actual price = $100 and predicted price = $120 <br>
SMAPE = |100-120| / ((|100| + |120|)/2) * 100% = 18.18% <br>

## Approach 

**Summary of My Approach**

I tested different ways to predict prices using product text and image data.

1) **BERT** gave the best results with the **lowest SMAPE score of around 47**. It clearly outperformed the other methods.

2) I also experimented with **ConvNeXt** to extract text information from image data.

3) In addition, I tried a **lightweight OCR** method using PaddleOCR to pull text from images.

Overall, BERT was the most accurate and reliable model in my experiments.


