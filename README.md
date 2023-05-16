
# Marketing Campaign Data Science

Sports Wear Group wants to leverage advanced analytics for boosting marketing campaigns. It is one of the leading retailers in the region, with more than 50 branches across the region. It runs multiple lines of business applications, mainly in the sport goods industry. They are in the middle of their digital transformation journey and they want to keep leading the market by satisfying their customers and meeting their expectations.
This data science project aims to help support the company.

**Business Environment and Goals:** Sports Wear Group will release an advanced analytics RFP.  Each of the vendors will be given a 30 min slot to present their analytics capabilities and the value that their technology presents in front of us; including the value from both a technical and business perspective. 
The first part of the meeting will include people from two teams, the marketing team and the management team. We want to see the value from using your platform for advanced analytics and the data platform challenges that accompany it. Given the data sample we provided from our sales databases, we want to know if using advanced analytics you can help the marketing team. While the marketing team will be interested to see if they can increase their efficiency, the management team wants to know if using advanced analytics may increase sales in general. 
Finally, for another 30 min, our data scientist team is interested in the data science process you are using and the details of the algorithm you are using to solve the proposed problem.
We are considering leveraging the cloud.  








## The Sales Data

The provided data represents information from a marketing campaign. We provided information about the product in the campaign/offer that was sent to a specific customer and the convergence result of this campaign (label attribute).  We provided you with every attribute we have about the product, use whatever you see makes sense to solve the defined project.

| attribute       |  Description                                        |
| :-------- | :-------                    |
| `country` | Country name                  |
| `article`| 6 digit article number, as unique identifier of an article       |
| `sales` | total number of units sold in respective retail week                    |
| `regular_price`  | recommended retail price of the article |
| `current_price`|current selling price (weighted average over the week) |
| `ratio`  | price ratio as current_price/regular_price, such that price discount is 1-ratio|
| `retailweek` | start date of the retail week |
| `promo1` | indicator for media advertisement, taking 1 in weeks of activation and 0 otherwise|
| `promo2`  | indicator for store events, taking 1 in weeks with events and 0 otherwise|
| `customer_id` | customer unique identifier, one id per customer|
| `product group`  | product group the article belongs to |
| `category` |product category the article belongs to |
| `cost`| total costs of the article (assumed to be fixed over time) |
| `style`   |description of article design |
| `sizes:` | size range in which article is available   |
| `gender`  | gender of target consumer of the article       |
| `rgb_*_main_color` |intensity of the red (r), green (g), and blue (b) primaries of the article‘s  main color, 		taking values [0,250]|
| `rgb_*_sec_color` |intensity of the red (r), green (g), and blue (b) primaries of the article‘s secondary 		color, taking values [0,250]|
| `label`   |advertisement result after offering/sending/presenting the offer to the customer. 0 means the customer did not buy and 1 means the customer did buy|


## Experiments

Applied different experiments of different models. As the data is unbalanced I took 2 approaches to upsample the data SMOTE and Random Over Sampler(unreliable as it probably will cause over fitting because it repets the data so the model will overfit)

| Model                             |  Upsampling Method          | Accuracy  |
| :--------                         | :-------                    | :-------  |
| `K-Nearest Neighbour(KNN)`        | Random Over Sampler         | 78.54 %   |
| `K-Nearest Neighbour(KNN)`        | SMOTE                       | 74.72 %   |
| `Decision Tree`                   | Random Over Sampler         | 84.82 %   |
| `Decision Tree`                   | SMOTE                       | 83.04 %   |
| `Random Forest `                  | Random Over Sampler         | 81.92 %   |
| `Random Forest`                   | SMOTE                       | 80.81 %   |
| `XGBoosting `                     | Random Over Sampler         | 98.97 %   |
| `XGBoosting`                      | SMOTE                       | 94.59 %   |

## How to Install and Run?

### Python environment requirements

```
pip install -r requirements.txt
```

### Sales Data 

Sales data is provided in the project repository to download and use.


### Clone the repository

```
  git clone https://github.com/username/repo.git
```

### Results Visualizations

Data visualized using Tableau, link for full story can be found [here](https://public.tableau.com/views/FinalTestDataScience/Story1?:language=en-US&:display_count=n&:origin=viz_share_link).


## Experiments

Applied different experiments of different models. As the data is unbalanced I took 2 approaches to upsample the data SMOTE and Random Over Sampler(unreliable as it probably will cause over fitting because it repets the data so the model will overfit)

| Model                             |  Upsampling Method          | Accuracy  |
| :--------                         | :-------                    | :-------  |
| `K-Nearest Neighbour(KNN)`        | Random Over Sampler         | 78.54 %   |
| `K-Nearest Neighbour(KNN)`        | SMOTE                       | 74.72 %   |
| `Decision Tree`                   | Random Over Sampler         | 84.82 %   |
| `Decision Tree`                   | SMOTE                       | 83.04 %   |
| `Random Forest `                  | Random Over Sampler         | 81.92 %   |
| `Random Forest`                   | SMOTE                       | 80.81 %   |
| `XGBoosting `                     | Random Over Sampler         | 98.97 %   |
| `XGBoosting`                      | SMOTE                       | 94.59 %   |
