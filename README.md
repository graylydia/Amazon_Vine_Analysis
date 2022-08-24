# Amazon Vine Analysis
## Overview of the Analysis
### Purpose
In this project, we were tasked with analyzing a chosen dataset of Amazon reviews. I chose to analyze the automotive reviews. The surveys were broken up by two main categories: members and non-members of the Amazon Vine program. This program provides feedback to manufacturers and publishers through the reviews and if you are a member then you are paid and required to provide feedback on the product. To analyze the dataset, we performed the Extract Transform Load process through PySpark, an AWS RDS instance, and pgAdmin. Then we examined any bias toward the products based on if the review was written by a member of the Vine program. 
## Results
<img width="699" alt="Vine_Reviews" src="https://user-images.githubusercontent.com/103657822/186449367-9797db9f-5e71-4b6a-8f3e-6fa44f577418.png">
<img width="475" alt="Vine_Total_Reviews" src="https://user-images.githubusercontent.com/103657822/186450050-697d13be-7fcc-4577-84de-11b798e8b34b.png">
<ul><li> The image above shows how we filtered our DataFrame through Pandas to select only the reviews written by a Vine member(paid). The total number of Vine reviews is 82. </li></ul>
<img width="737" alt="non_Vine_Reviews" src="https://user-images.githubusercontent.com/103657822/186450702-863282c2-f26c-4818-b3b9-721d50716a91.png">
<img width="507" alt="non_Vine_Total_Reviews" src="https://user-images.githubusercontent.com/103657822/186450720-e671e944-bb5c-4662-bfa2-d5ff7a99706f.png">
<ul><li> Now we have filtered our Pandas DataFrame to select only non-Vine member(unpaid) reviews. There were a total of 24,742 non-Vine reviews. </li></ul>
<img width="812" alt="Vine_Five_Star" src="https://user-images.githubusercontent.com/103657822/186451687-62cda472-fa72-48ef-9e9a-ac1efafa1982.png">
<img width="645" alt="Vine_Percentage" src="https://user-images.githubusercontent.com/103657822/186452457-bd0a81d5-3fd7-4026-9de3-ee372a3666b3.png">
<ul><li> Only 33 out of the 82 Vine reviews were 5 stars. We can conclude that only 40.24% of Vine reviews were 5 stars. </li></ul>
<img width="854" alt="non_Vine_Five_Star" src="https://user-images.githubusercontent.com/103657822/186451948-ac733466-e1e8-4c54-b294-c2e6ca5d2ba8.png">
<img width="695" alt="non_Vine_Percentage" src="https://user-images.githubusercontent.com/103657822/186453211-bdfc1d95-9ecd-4fde-a8a2-084d939c7bf4.png">
<ul><li> 12,807 out of the 24,742 non-Vine members gave a 5 star review. As a result, 51.76% of the non-Vine member reviews were 5 stars. </li></ul>

## Summary
You would think there would be a drastic difference between member and non-member reviews since members are being paid. However, there isn't any positivity bias for reviews in the Vine program for the automotive products. Less than half of the Vine reviews were 5 stars (40.24%). Whereas, non-Vine members gave a higher rating with 51.76% 5 star reviews. There is an 11.52% difference in five star reviews between member and non-members of the Vine program. Additionally, we see that there are more non-member reviews than member reviews. An additional analysis that we could perform is to find the mean of member and non-member reviews. Finding the mean would give more insight to any biases found in the reviews.  
