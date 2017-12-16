# E4571 Personalisation Theory Class Project  -- Fall 2017

<br>

**Team Members:**

<table>
<tr>
  <td>Name</td>
  <td>GitHub</td>
  <td>UNI</td>
</tr>
<tr>
  <td>Tejas Dharamsi</td>
  <td>https://github.com/Dharamsitejas</td>
  <td>td2520</td>
</tr>
<tr>
  <td>Abhay S Pawar</td>
  <td>https://github.com/abhayspawar</td>
  <td>asp2197</td>
</tr>
<tr>
  <td>Janak A Jain</td>
  <td>https://github.com/janakajain</td>
  <td>jaj2186</td>
</tr>
<tr>
  <td>Vijayraghavan Balaji</td>
  <td>https://github.com/vijaybalaji30</td>
  <td>vb2428</td>
</tr>
</table>


<hr>
<br>
~Steps to run the code~

- Clone/Download the Repository
- install dependencies `pip3 install -r requirements.txt`
- move to folder Part1/analysis.
- Execute CF-Data.ipynb notebook


> Report for Part 1 of the project can be found in [Part1/documents/report_part1.pdf](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/Part1/documents/report_part1.pdf)
  
> Note: The main file containing the code is [CF-Data.ipynb](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/Part1/analysis/CF-Data.ipynb)


### File Structure

#### Top
* Part1
    - [analysis](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/tree/master/Part1/analysis): CF-Data.ipynb main part1 file along with exploratory stuff.
    - [clean-data](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/tree/master/Part1/clean-data): Contains subset smaller datasets
    - [raw-data](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/tree/master/Part1/raw-data): Contains book-crossing raw datasets.
    - [documents](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/tree/master/Part1/documents): instructions and report
    - [figures](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/tree/master/Part1/figures): Contains Plots for visualisation
* Part2
    - [Final_Project_Outline.pdf](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/Part2/outline.pdf)
    - analysis  
      + _DatasetCreation\_Benchmark\_ContentBased.ipynb_: contains the code for combination of dataset, Naïve baseline model, item-item collaborative filtering model and content based model
      + _LSH_Complete.ipynb_: contains the code for LSH model
      + _book\_features.ipynb_: contains the code for generating word2vec features for books

    - created\_datasets      		
      + _Combine.csv_ : contains the combined dataset of BX and Amazon dataset  
      + _book_features.csv_: contains the data with features generated using word2vec     
      + _ibsn_features_new_batch.pickle_: contains the data with features extracted BookReads API and enriched using word2vec  
      
    - Goodreads Merged Features.ipynb
* License
* Readme
* requirements.txt


# About the Project  
  
![Book Shelf Image](http://www.wellbuiltstyle.com/wp-content/uploads/2015/12/library.jpg)  
_Image Courtesy: WellBuiltStyle.com_  

  
The project is part of the course on [Personalization Theory and Applications](https://ds-personalization.github.io/class/) by [Prof. Brett Vintch](http://www.cns.nyu.edu/~vintch/). The aim of this project is to create a recommender system for books that is capable of offering customized recommendations to book readers based on the books they have already read.


## Motivation  

> _There is no friend as loyal as a friend - Ernest Hemingway_

Thanks to [Gutenberg](https://en.wikipedia.org/wiki/Johannes_Gutenberg) and now, the digital boom, we now have access to a huge amount of collective intelligence, wisdom and stories. Indeed, humans perish but their voice continues to resonate through humans brains and minds long after they are gone - sometimes provoking us to think, making us parts of revolutions and sometimes confiding in us with their secrets. They have the ability to make us laugh, cry, think - think hard, and most imporantly, change our lives the way, perhaps nobody else can. In this sense, books are truly our loyal friends.

Can the importance of books as loyal friends ever be overestimated? We think not. Which is why we think that creating just the 'right' recommendations for readers is a noble objective. Consider it a quieter (Shh.. no noise in this library! :)) Facebook or a classier Tinder for those who like to read and listen, patiently.
  
---  
  
## Part II - Summary of findings 

We have implemented four different types of algorithms from scratch and have compared them with with a naïve model. These four models are Tree-based Approximate Nearest Neighbor (ANN), Locality Sensitive Hashing (LSH), Item-item collaborative filtering (CF) and Content-based model. We also created a hybrid model that is a combination of LSH and Content-based model.

We used five-fold cross-validation for all of our developed models, which helped us in selecting the best model for comparison against the benchmark.

We have evaluated each of the developed models on following evaluation metrics:
- Training time
- RMSE
- MAE
- Coverage
- Novelty
 
**Results**:  
  
<table>
  <caption><b><i>Comparison of several models on various comparison metrics</b></i></caption>
  <tr>
    <th>Model Name</th>
    <th>Training Time (hours)</th>
    <th>Best K</th>
    <th>Average Test MAE</th>
    <th>Average Test RMSE</th>
    <th>Coverage</th>
  </tr>
  
  <tr>
    <td><b>Naïve</b></td>
    <td>N/A</td>
    <td>n/a</td>
    <td>0.763</td>
    <td>0.944</td>
    <td>N/A</td>
  </tr>
  
  <tr>
    <td><b>Item-item CF</b></td>
    <td>4.1</td>
    <td>15</td>
    <td>0.553</td>
    <td>0.759</td>
    <td>76.0%</td>
  </tr>
  
  <tr>
    <td><b>Tree based ANN</b></td>
    <td>1.927</td>
    <td>20</td>
    <td>0.55</td>
    <td>0.76</td>
    <td></td>
  </tr>
  
  <tr>
    <td><b>LSH</b></td>
    <td>1.29</td>
    <td>15</td>
    <td>0.573</td>
    <td>0.796</td>
    <td>65.6%</td>
  </tr>
  
  <tr>
    <td><b>Content-based</b></td>
    <td>0.5 (approx.)</td>
    <td>25</td>
    <td>0.593</td>
    <td>0.8031</td>
    <td>31.55%</td>
  </tr>
  
  <tr>
    <td><b>Hybrid (LSH + Contentt)</b></td>
    <td>1.79</td>
    <td>15</td>
    <td>0.5834</td>
    <td>0.799</td>
    <td>46.54%</td>
  </tr>
  
</table>
  
### Tweaking the Hybrid model  
  
After developing the Hybrid model from scratch, the next step for us was to evaluate it different values of its hyper-parameter - the distribution of weights on the two underlying models. Given below is a summary of the MAE and RMSE metrics for the Hybrid model for various combinations of these weights.

<table>
  <caption><b><i>Performance of the Hybrid model for various weight combinations of the underlying models</b></i></caption>
  <tr>
    <th>W_LSH</th>
    <th>W_Content</th>
    <th>MAE</th>
    <th>RMSE</th>
  </tr>
  
  <tr>
    <td><b>0.9</b></td>
    <td>0.1</td>
    <td>0.587</td>
    <td>0.813</td>
  </tr>
  
  <tr>
    <td><b>0.8</b></td>
    <td>0.2</td>
    <td>0.585</td>
    <td>0.806</td>
  </tr>
  
  <tr>
    <td><b>0.7</b></td>
    <td>0.3</td>
    <td>0.583</td>
    <td>0.799</td>
  </tr>
  
  <tr>
    <td><b>0.6</b></td>
    <td>0.4</td>
    <td>0.583</td>
    <td>0.796</td>
  </tr>
  
  <tr>
    <td><b>0.5</b></td>
    <td>0.5</td>
    <td>0.583</td>
    <td>0.792</td>
  </tr>

</table>

### Interpretations  
  
We selected the Hybrid model with a W\_lsh to W\_content weight ratio of 7:3 in order to select the right blend of coverage and serendipity. However, we observed that even at this level, the coverage of the model was significatly lower than that of the LSH model that we implemented from scratch. Hence, we would recommend the use of LSH model for making recommendations.  
  
### Future Scope of Work  
  
In the future, we would like to extend this study to convert our code into a Python package and publish a paper on the same. We invite members of the larger academic community to contribute to this project.
  
---

## Part I - Summary of findings 

We have implemented two different types of algorithms from scratch and have compared them with competitive models available from other packages. These two algorithms are Item-Item Collaborative Filtering and  Non-negative Matrix Factorization (NMF)

We implemented our models using two approaches:
 - Collaborative filtering based (Approach 1)
 - Non-negative Matrix Factorization (NMF)based (Approach 2)

We used cross-validation for all of our developed models, which helped us in selecting the best model for comparison against the benchmark.

For both these approaches, we implemented two separate models for this study - one model was developed from scratch, while one was developed using [Surprise](http://surpriselib.com/). 
 
**Results**:  
  
- For Approach 1, our model performed better than Surprise model for by a significant measure for Average MAE. 
- For Approach 2, our model did not fare well in front of Surprise model.

For each approach the results are described below below for each of the norms, viz. **Euclidean distance**, **cosine distance** and **pearson correlation coefficient**:

### Approach 1: Item-Item Collaborative filtering based
  
  
<table>
  <caption><b><i>Euclidean distance</b></i></caption>
  <tr>
    <th>Model Name</th>
    <th>Average RMSE</th>
    <th>Average MAE</th>
  </tr>
  <tr>
    <td><b>Our model</b></td>
    <td>1.54</td>
    <td>0.96</td>
  </tr>
  <tr>
    <td><b>Suprise</b></td>
    <td>1.58</td>
    <td>1.13</td>
  </tr>
 </th>
</table>
  
<table>
  <caption><b><i>Cosine similarity</b></i></caption>
  <tr>
    <th>Model Name</th>
    <th>Average RMSE</th>
    <th>Average MAE</th>
  </tr>
  <tr>
    <td><b>Our model</b></td>
    <td>1.57</td>
    <td>1.06</td>
  </tr>
  <tr>
    <td><b>Suprise</b></td>
    <td>1.64</td>
    <td>1.22</td>
  </tr>
 </th>
</table>


<table>
  <caption><b><i>Pearson correlation coefficient</b></i></caption>
  <tr>
    <th>Model Name</th>
    <th>Average RMSE</th>
    <th>Average MAE</th>
  </tr>
  <tr>
    <td><b>Our model</b></td>
    <td>1.53</td>
    <td>1.01</td>
  </tr>
  <tr>
    <td><b>Suprise</b></td>
    <td>1.61</td>
    <td>1.20</td>
  </tr>
 </th>
</table>

---  

### Approach 2: None-negative Matrix Factorization
  
  
<table>
  <caption><b><i>NMF</b></i></caption>
  <tr>
    <th>Model Name</th>
    <th>Average RMSE</th>
    <th>Average MAE</th>
  </tr>
  <tr>
    <td><b>Our model</b></td>
    <td>2.97</td>
    <td>2</td>
  </tr>
  <tr>
    <td><b>Suprise</b></td>
    <td>1.53</td>
    <td>0.98</td>
  </tr>
 </th>
</table>
  


  
## Feedback  
  
We look forward to your feedback and comments on this project. Our email IDs are a combination of our four-letter UNI codes e.g. 'td2520' and follow the following rule: {UNI}@columbia.edu.
