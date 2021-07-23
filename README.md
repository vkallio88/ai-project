# Calculating IT support ticket urgency based on words used in description

Final project for the Building AI course

## Summary

This is a pretty simple idea and someone has probably done something like this, but here goes. The idea is to gather information about a new IT support ticket, which is not in progress yet and use algorithm/algorithms to estimate the urgency of a ticket based on words used in the Description section of the support ticket.


## Background

In our IT department, it is sometimes hard to know which support tickets are urgent and which are not, especially during rush hours. The thing we have realised is that we can usually (but not always) predict the urgency of a ticket based on words used in the Description. Sure, predictions will not be 100% accurate, but that is not a problem. Biggest problem at the moment is the fact that urgent cases tend to pile up in the system. This hopefully helps to draw attention to these urgent cases.


## How is it used?

Process could go something like this:
- Poll database/API for new tickets with no classification or handler
- Use relevant method with Python to classify words  to "urgent" and "non-urgent" categories. If there are more "urgent" words than "non-urgent" words, then ticket is classified as "urgent" and vice versa.

Users are IT support system admins and IT support personnel. Their need is to get the information about a potential urgent ticket as soon as possible (this has always been a problem), especialy since most of the ticket are NOT logged by the support personnel, but rather by customers.

## Data sources and AI methods

Our integration specialists will collect the ticket data from system via API call or database query. So the data is gathered from IT ticket system, and actually, this kind of ticket data is already gathered, we just do not use it that efficiently.

Since this is a pretty simple case with words, maybe Naive Bayes classifier could be used as a starting point. Maybe later, when expanding the solution to do more classifications and forecasts with words could the Term Frequency Inverse Document Frequency (tf-idf) technique be used. This could be the ultimate technique of choice for this, since we could use older/earlier tickets as a training data for the algorithm. As you can see, I am not a programmer, so this description is pretty vague.

## Challenges

I suppose the biggest limitation is the data. If the description are short and off-point, then this all amounts to nothing. So, there should be some kind of a template when submitting a ticket, just to make sure all the relevant information is (forcefully) gathered. Nevertheless, problems and inconsistencies with data will most likely still occur.

This project only tries to solve this very spesific problem and really nothing else. This is my first crack at trying to understand the subject matter, so bear with me.

## What next?

Well, we do have data scientists and integration specialist here, so I will probably seek their help with this and hopefully understand the whole process a lot better. This is not probably a very hard project for a data scientist and/or a integration specialist.

## Acknowledgments

Thanks the Elements of AI Team for the knowledge and inspiration. Keep up the good work!
