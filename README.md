# Hotel_Reviews_Analysis

Ever wonder why you have certain promotion while your friends don't receive any? This business strategy is called personalized marketing. The goal of personalized marketing is to attract prospective customers and retain loyal customers. 

### Project Goal:
If you are someone who loves travelling like me, then you are probably familiar with the struggle of booking a good hotel. Here’s an example. You might see a five rating stars hotel on TripAdvisor, however, after your stay, you are disappointed because your expectations doesn’t match with the reality. While TripAdvisor does have ratings for things like location, service etc, it can be difficult to fully capture a hotel’s pros and cons. So, I was inspired to build a hotel pros and cons model to help end users like us to make booking decisions easier. 

### Project Workflow:
First, I cleaned the review data, and only keeping the adjective and noun words. After that, I separate positive reviews and negative reviews based on customer ratings. Lastly, I use count vectorizer with ngram range 2 to 3 to create a bag of words. Then, I build a logistic regression model. Based on the beta coefficient on the bag of words, we only extract the top 10 positive and negative words from the model. 

On top of that, I ran a topic modeling on only the positive words, and use the cosine similarity to find the most similar hotels based on their pros.

I used Tableau to create a demo. In the Tableau app, each dot represents a hotel. The size of the dot is correlated with the number of reviews they have. So essentially, how popular they are. In this graph, I used the 2016 household income census data to separate the neighbourhood. So the darker the purple is, the wealthier the neighbourhood the hotel is in. Let’s say if you are satisfied with a hotel you stayed before like this Sheraton Seattle Hotel. You liked the cleanliness and the location of the hotel, however you are not satisfied with their service. So with the recommendation filter, now we are able to compare hotels that have similar pros. We can hover over to see another hotel’s pros and cons. This hotel is in a richer region, and as we can see it here, the staff are helpful. Most importantly, the cleanliness and the location are still very good. However, be aware that the room might be noisy and it might take some time to get a reservation. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/y1ZWIbgna1A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

As you can tell, from this demo, imploying nlp technique and logistic regression to extract pros and cons can give great results. The technique I used here can be applied to pretty much anything that has reviews data. we can not only help the users make decision on any ecommerce site, we can also help suppliers gain more informative feedback so that they can make improvements. Also, we can help the dis’-tri-butors to increase customer retention rate by building a more user friendly platform. Happy users, happy companies. win win!


### Install

This project requires **Python** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [sklearn](https://scikit-learn.org)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)


### Run

In a terminal or command window, navigate to the top-level project directory and run one of the following commands:


```bash
01-TripAdvisor-Data-Import.ipynb	
02-TripAdvisor-Data-EDA.ipynb
03-Building-Logistic-Regression-Model.ipynb
04-Topic Modelling & Cosine Similarity.ipynb
```

This will open the Jupyter Notebook software and project file in your browser.

#### Data:
I got this dataset from a PhD NLP researcher’s website. He webscrapped 878,561 reviews from 4333 hotels crawled from TripAdvisor. Since it might take a long time to run the model, I narrow my scope down, and only look at the reviews from Seattle hotels. 


