# Part I - Description  
  
---  
## Domain and Dataset  
  
Books are an important part of a person's life. They cheer, educate and connect us in ways nothing else can. Readers are often on the lookout for meaningful and relevant recommendations. It is in this spirit of enquiry that we have decided to work on the problem of coming up with a recommender system that resolves this problem while offering to personalize the experience for its users. The dataset that we have picked is the [BX books dataset ](http://www2.informatik.uni-freiburg.de/~cziegler/BX/) which contains details on around 170,000 books and 100,000 users.  
  
---  
## Business Case  
  
### Vision  
Our vision is to connect readers with the most _**contextually relevant**_ and _**meaningful**_ recommendations for books.  
  
### Mission  
We plant to achieve our vision through the following mission plan:  
1. **Understanding aspirations and motivations of our readers**:  This will inform the design and modeling decisions of our recommender system so that it works as per a given context. Indeed, user needs are not constant - they not only change over time, but it is possible that the same user would need different recommendations for different times of the year, month or even day. While we understand that modeling this can be a big design challenge, inclusion of this factor in our approach at least in design thinking terms can help us make the right design choices if not model them directly.  
  
2. **Meaningul recommendations**: The term meaningful needs careful delineation at the very onset - by 'meaningful',  we mean the recommendations that are not just intelligently relevant, but instinctively relevant. This is central to the recommender system which models choices for readers who just do not always want the expected choices. This corresponds to both the concepts of [Situational Equity](http://www.tnsglobal.com/what-we-do/by-expertise/brand-communication/brand-communication/situational-equity) propounded by Kantar TNS and the needs hierarchy, viz. stated, real, unstated, delight and secret needs. In this project, we shall not target secret needs as that requires the kind of data that can be very expensive to collect, we wish to allude to its importance.  
  
---  

### User  
We use the term _**user**_ to describe any person who seeks recommendations for books. He/she may be a new or avid, casual or involved reader.  
  
---  
## Sampling from the dataset  
  
From the chosen dataset, we have selected records for 10,000 users and ~100 books for recommendations.  
  
---  
## Building two brute-force collaborative filtering algorithms:  
	1. Neighborhood based: For this approach, we have decided to use user-based collaborative filtering that as we believe there are certain dominant patterns related to personality of users who liek similar books.  
	2. Model-based: 
  
