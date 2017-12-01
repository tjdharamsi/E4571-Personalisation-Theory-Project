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
  - License
  - Readme
  - requirements.txt

<hr>

# About the Project  
  
![Book Shelf Image](http://www.wellbuiltstyle.com/wp-content/uploads/2015/12/library.jpg)  
_Image Courtesy: WellBuiltStyle.com_  

  
The project is part of the course on [Personalization Theory and Applications](https://ds-personalization.github.io/class/) by [Prof. Brett Vintch](http://www.cns.nyu.edu/~vintch/). The aim of this project is to create a recommender system for books that is capable of offering customized recommendations to book readers based on the books they have already read.
  

## Motivation  

> _There is no friend as loyal as a friend - Ernest Hemingway_

Thanks to [Gutenberg](https://en.wikipedia.org/wiki/Johannes_Gutenberg) and now, the digital boom, we now have access to a huge amount of collective intelligence, wisdom and stories. Indeed, humans perish but their voice continues to resonate through humans brains and minds long after they are gone - sometimes provoking us to think, making us parts of revolutions and sometimes confiding in us with their secrets. They have the ability to make us laugh, cry, think - think hard, and most imporantly, change our lives the way, perhaps nobody else can. In this sense, books are truly our loyal friends.

Can the importance of books as loyal friends ever be overestimated? We think not. Which is why we think that creating just the 'right' recommendations for readers is a noble objective. Consider it a quieter (Shh.. no noise in this library! :)) Facebook or a classier Tinder for those who like to read and listen, patiently.

  
## Approach  

In this project, we shall use a hybrid approach in creating the recommender algorithm which is based on both content-based and context-based collaborative filtering. This will give the recommender system a nice balance.


## Part I - Summary of findings 
  
We implemented our models using two approaches:
 - Collaborative filtering based (Approach 1)
 - Non-negative Matrix Factorization (NMF)based (Approach 2)

We used cross-validation for all of our developed models, which helped us in selecting the best model for comparison against the benchmark.

For both these approaches, we implemented two separate models for this study - one model was developed from scratch, while one was developed using [Surprise](http://surpriselib.com/). 
 
**Results**:  
  
- For Approach 1, our model performed better than Surprise model for by a significant measure for Average MAE. 
- For Approach 2, our model did not fare well in front of Surprise model.

For each approach the results are described below below for each of the norms, viz. **Euclidean distance**, **cosine distance** and **pearson correlation coefficient**:

#### Approach 1: Item-Item Collaborative filtering based

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



#### Approach 2: None-negative Matrix Factorization

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
    <td>0.98</td>
    <td>1.53</td>
  </tr>
 </th>
</table>
  

## Code

#### Steps to run the code

- Clone/Download the Repository
- install dependencies `pip3 install -r requirements.txt`
- move to folder Part1/analysis.
- Execute CF-Data.ipynb notebook


> Report for Part 1 of the project can be found in [Part1/documents/report_part1.pdf](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/Part1/documents/report_part1.pdf)
  
> Note: The main file containing the code is [CF-Data.ipynb](https://github.com/Dharamsitejas/E4571-Personalisation-Theory-Project/blob/master/Part1/analysis/CF-Data.ipynb)

  
## Feedback  
  
We look forward to your feedback and comments on this project. Our email IDs are a combination of our four-letter UNI codes e.g. 'td2520' and follow the following rule: {UNI}@columbia.edu.
