---
layout: post
title: Exploring Reviews of Airline Services
---

In current times, a lot of user generated content can be found on the internet. One specific type of content that has proven to be extremely useful and interesting to people are reviews. Most of the time, when buying a product or service people tend to read reviews to find out if it is worth buying at all. This is also true when dealing with airline services.

This post will explore a dataset that was created by scraping an online airtravel review site owned by [Skytrax](http://www.airlinequality.com/). Skytrax is also the company that produces a yearly list of the best airlines in the world. This list is often covered by the media ([CNN](http://edition.cnn.com/2015/06/16/travel/skytrax-best-airlines-awards-2015/), [Business Insider](http://uk.businessinsider.com/the-20-best-airlines-in-the-world-according-to-skytrax-2015-6?r=US&IR=T), [Entrepeneur](https://www.entrepreneur.com/slideshow/247489)) and can thus be easily found when doing a simple Google [search](https://www.google.nl/search?q=best+airlines+in+the+world&oq=best+airlines+in+the+world&gws_rd=cr&ei=x7AxV7P8F4XxUrmjtNgG).
Naturally, a lot of criteria needs to be considered when producing such a list. An important aspect should of course be customer satisfaction. Potential future customers tend to consult this ranking list to quickly find out if the airline they want to travel with is in fact a good one. So the question that is going to be answered in this post is:

> Does Skytrax’ list of best airlines in the world reflect the customers satisfaction?

## Dataset

The dataset that is used in this post can be found [here](https://github.com/quankiquanki/skytrax-reviews-dataset) on my Github account. The dataset was scraped and created on August 2, 2015. Reviews are categorised into 4 main groups and in total there are:

* 41396 Airline Reviews
* 17721 Airport Reviews
* 1258 Seat Reviews
* 2264 Lounge Reviews

Information such as the airline, airport, text content, dates as well as ratings and any sub-ratings are also found in this dataset. More details of this dataset can be found on the Github page.

## Exploration and Visualisation

Even though the dataset contains a lot of information, this blog post will only scratch the surface of it. Let us first find out who the reviewers are. Where do the Skytrax reviewers come from? This can be best shown using a world map.

<iframe id="plotly-quankiquanki:101" width="100%" height="480" frameborder="0" scrolling="no" src="https://plot.ly/~quankiquanki/101.embed" style="max-width: 100%;"></iframe>

Exploring the visualisation shows that the reviews are mostly coming from countries where people speak English such as America and Australia. The most reviews originate from England, this could be due to Skytrax being an English company. There are also small amounts of reviewers coming from Europe and the Eastern part of Asia. Also note that all reviews on the Skytrax website are written in English which can further explain the amount of English speaking reviewers. The overall user rating about an airline, airport, seat or lounge is reflected on a scale of 1 to 10. This can be visualised as a bar chart for each of the main category in the dataset.

<iframe id="plotly-quankiquanki:278" width="100%" height="480" frameborder="0" scrolling="no" src="https://plot.ly/~quankiquanki/278.embed" style="max-width: 100%;"></iframe>

Similar to the world map, this bar chart is also interactive. It is possible to use the legend to show or hide any type of category just by clicking on it. By default, only the airline ratings are shown. Note that most users tend to give an airline either a very low rating or a very high rating. Fortunately for the airlines, the distribution is skewed towards the positive side. However, the other categories are all heavily skewed towards a low rating. People do not seem to be very satisfied about the airports, lounges and seats.

Now that it is somewhat known where the users are from and what their overall opinions are, it is time to find out which are in fact the most customer satisfying airlines in the world. More interestingly, how does this data compare to the airline rankings that Skytrax published in 2015. This comparison is shown with the next visualisation.

<iframe src="https://plot.ly/~quankiquanki/674/.embed" width="100%" height="480" frameborder="0" scrolling="no" seamless="seamless"></iframe>

This scatter plot shows the average rating of each airline in the dataset. It also shows how many reviews each airline has. The more reviews the more likely that the rating is indeed the general opinion. Also, airlines with less than 100 ratings were left out of this visualisation. The best airlines according to Skytrax are numbered from 1 to 20 based on their position on the ranking list.

Exploring the plot shows that the best customer satisfying airlines in the world are mostly from countries in Southeast and East Asia. The second best regions are the Middle-East and Europe. The worst airlines are mostly from the USA and Canada.

More interestingly, some of Skytrax’ best airlines are indeed also rated very high amongst the reviewers (e.g. Asiana Airlines and Garuda Indonesia). However, there are also major differences. Etihad Airways seems to be rated extremely low but Skytrax puts them in the 6th position of their ranking list. Air France, which is ranked 15, is also rated poorly amongst their customers. This makes you wonder how Skytrax’ ranking process actually works. Customer satisfaction based on the reviews from their own website do not seem to play a big part in their evaluation. Also looking at the spread of Skytrax’ best airlines, there is likely a good chance that a customer consulting this list would have been more satisfied when picking another airline.

## Conclusion

Comparing the overall ratings of the airline reviews in this dataset with Skytrax’ best airlines in the world shows an indication that customer satisfaction does not play a great role in Skytrax’ evaluation. Note that Skytrax’ ranking list of 2015 was used in this blog post, it can thus be said that only airline reviews from the year 2014 and maybe 2015 should have been used to compare them. Almost similar results were achieved when doing [this](https://plot.ly/~quankiquanki/695/comparing-skytrax-top-20-airlines-against-all-the-others-2014-2015-source-airlin/).

If being satisfied is one of your big concerns when flying with an airline, it is best not to consult Skytrax’ ranking list but rather look at the reviews from your fellow customers. So to put an end to the exploration of this dataset, it is time to show the chart that contains the best airlines in the world according to their customers overall ratings. It does not add a lot of additional information compared to the previous plot but this one is more pleasing to the eye if you are only interested in the best airlines.

<iframe src="https://plot.ly/~quankiquanki/558/.embed" width="100%" height="640" frameborder="0" scrolling="no" seamless="seamless"></iframe>

## Update

**31-08-2015:** The people at Priceonomics have used the same dataset to find out what the best and worst airports in the world are. So read on if you are interested in [that](http://priceonomics.com/what-are-the-worst-airports-in-the-world/).  
**01-09-2015:** A follow-up post about the best and worst full-service airlines in the world can be found [here](http://www.quangn.com/the-best-and-worst-full-service-airlines-in-the-world/).