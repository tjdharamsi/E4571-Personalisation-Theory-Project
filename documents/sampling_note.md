# A note on sampling  
  
The Books dataset used for this dataset is very sparse. Moreover, it has some inherent peculiarities which make the sampling process very tricky.  
  
These are described in detail below:  

1. Top books vs. Top users: As it appears, not all top users are associated with top books. This makes it difficult to select a sample that is appropriately dense while containing the data with the required number of users and books at the same time. For example, selecting the top user alone creates a dataset containing more than 100 books.
2. Representation: Carrying forward 1, we can also see that selecting a subset of users that excludes the top users, makes the recommendation problem restricted to a particular subset of users making this a recommendation exercise for a specific target groups (say, involved but not engaged users).

Problem 2 is dependent on the constraints and not inherent, so we shall ignore this for the purpose of Phase I. We shall however attempt to use a stratified sample for Phase II to ensure that it the resulting model is generalizable and representative.

![User Composition](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/figures/user_composition.png)

Based on the current arbitrary classification of users based on the numbers of books they have rated, we can see that there are fewer engaged users, while involved and casual users form a huge chunk of the user-base.