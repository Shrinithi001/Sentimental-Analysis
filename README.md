# Sentimental-Analysis
from textblob import TextBlob
f=open("feedbackdata.txt","r")
for line in f:
    print(line)
    obj=TextBlob(line)
    sentiment=obj.sentiment.polarity
    if(sentiment<0):
        print("Negative\n")
    elif(sentiment==0):
        print("Neutral\n")
    elif(sentiment>0):
        print("This sentence is Positive\n")
