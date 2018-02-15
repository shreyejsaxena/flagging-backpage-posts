# Tackling Trafficking on Backpage
Utilizing text analytics methods to identify potentially illicit sex-trafficking posts on Backpage

Our team collected and analyzed recent Backpage postings in efforts to identify potential patterns of online sex trafficking. Backpage is a classified advertisements website where individuals can sell products or services to others, or alternatively, make personal connections. Unfortunately, these websites have also been used to traffic unwilling sex workers. We are particularly interested in analyzing potential patterns of known coded words, emojis, descriptions, ages, ethnicities, and locations, among other possible insights, within our clusters of interest. 

Since there is no provided API for Backpage, we will apply alternative web scraping methods to collect all posts within each of the websites’ Women seeking Men section for major cities in California (San Francisco, Los Angeles, San Diego, etc).  

We had two main challenges in this analysis: 
1.	Performing stop word removal, stemming, and phrase clustering on short posts that may not be grammatically correct, that may not use correct spelling, that contain numerous abbreviations, etc.
2.	Differentiating posts that contain known coded words used in a potential trafficking context versus posts that contain the same words used in a different context 

Preparing the scraped posts for analysis required extensive and creative data cleaning. Posts often used confusable homoglyphs to prevent traditional text analytics methods from working, and often lacked grammatical structure. The python file within this directory shows how we identified non-latin characters and reassigned them to their most-similar latin counterparts. 

Our team also found success by performing clustering and topic analysis seperately on post emojis, post title, and post description, using each as a separate indicator of criminal activity. We used SAS Enterprise Miner to perform analysis on the collected documents. If we saw a known trafficking code-word or emoji within one of our clusters, we would consider that cluster to be a "red flag". The more red flags that a given post was a member of, the more we considered it to be at risk for criminal activity. 


The contained presentation summarizes our methodology, and included Excel sheets represent our results. 
