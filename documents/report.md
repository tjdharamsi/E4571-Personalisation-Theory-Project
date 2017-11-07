# Reado - A personalized book recommender system

## Case Study

### Story
Milton Keynes lives in England and like almost any other 29 year old, he is finally in a place in his life where he has a job that pays the bills, a nice place to stay and finally some time that he can use to focus on his hobbies. Milton likes reading -but just not like any other person, he loves reading so much so that he has a small library in his house where he spends about 4 hours on average everyday! He has already read and reviewed about 450 books. Now, that is something you don't expect a typical 29 year old. But Milton is not alone. There are many others like him, who like to have conversations with their favourite books. It wouldn't be an exaggeration to say that they live partly in a different dimension (fiction lovers will like this). 

As it so happens, Milton's best friend Jake can't stop thinking about using the data on these ratings to find people similar to Milton and creating a recommendation algorithm that generates a list of books that he should read. This would make a great birthday gift for Milton - for a birthday which is not far! But the problem is much complex than it seems. 

_Firstly_, the data is extremely sparse. [MORE DATA HERE]  
_Secondly_, the definition of similarity is very vague. How do we characterize similarity? How do we select similar entities?

**Note**:In this case study, we shall cover these as well as other pertinent aspects that can inform the solution. We also take a step-by-step approach in explaining our approach to elucidate our work to the diverse set of readers. We welcome any feedback and/or questions from our readers.

### Business Perspective
#### Motivation
Thanks to Gutenberg and now, the digital boom, we now have access to a huge amount of collective intelligence, wisdom and stories. Indeed, humans perish but their voice continues to resonate through humans brains and minds long after they are gone - sometimes provoking us to think, making us parts of revolutions and sometimes confiding in us with their secrets. They have the ability to make us laugh, cry, think - think hard, and most imporantly, change our lives the way, perhaps nobody else can. In this sense, books are truly our loyal friends.

Can the importance of books as loyal friends ever be overestimated? We think not. Which is why we think that creating just the 'right' recommendations for readers is a noble objective. Consider it a quieter (Shh.. no noise in this library! :)) Facebook or a classier Tinder for those who like to read and listen, patiently.
#### Vision
To provide ***meaningfully relevant*** book recommendations for readers based on their readership data.
#### Mission
We aim to achieve our vision through a systematic process which is given below:
1. **Meaningful**: The recommendations have to be something that the user is expected to find useful. Usefulness in this context can have several definitions in terms of genre, publisher, author etc. We begin with an assumption that similar people read and rate similar books and hence this similarity becomes a good discriminant for selection.
2. **Relevant**: There has to be a measurable performance that can represent the relevance of a recommendation. On a ten-point scale, we would not want the estimated ratings to be "off" by more than one point on the scale. For this our target RMSE is less than 1.00 (for a ten point scale) which translates to less than 0.5 for a 5 point scale.
3. **Exciting**: We would want out recommendations to have an element of serendipity - indeed, a recommendation is more meaningfully relevant if it excites the user (which is the ultimate objective). This approach would require more data and we intend to enrich our data and attempt to factor in this requirement in Phase II of our project.

### Objective
We are trying to optimize on several parameters:
1. **RMSE**: It is important that the estimated ratings do not have a large variance to the extent that their relative rankings are affected. For this purpose, an ideal RMSE threshold has been fixed as mentioned above.
2. **MAE**: Along with optimal RMSE, we would also focus on optimizing MAE (Mean Absolute Error).
2. **Serendipity**: Although this is more subjective , it is a very important component in making a recommendation meaningfully relevant. We shall attempt to characterize, determine and measure this component in Phase II.

In our pursuit to provide meaningfully relevant book recommendation to readers, we are willing to compromise on the following:
1. **Absolute rating estimates**: Below a certain threshold, our approach would not aim to improve absolute rating values. As mentioned before, for the algorithm, the relative rankings are more important and we aim to keep a control on this based on the defined RMSE threshold.
2. **Right vs. correct**: We would be ready to compromise correct recommendations for right recommendations. Correct recommendations would be the ones calculated without factoring in serendipity. Right recommendations might not include all the correct recommendations but would have a higher relevance. We aim to explore this factor more in Phase II.
### Approach
Following the directions mentiond in the [instructions](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/documents/mini_project_instructions.pdf), we shall do the following:
1. **Sampling** an appropriate dataset that contains <10,000 users and <100 items. The reader is advised to read our [note on sampling](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/documents/sampling_note.md).
2. 
#### Sampling
As specified in the [instructions](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/documents/mini_project_instructions.pdf) document, we have to select a sample of 
