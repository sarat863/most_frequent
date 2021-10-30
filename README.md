# most_frequent
import operator 
def most_frequent(str):
    d=dict()
    for key in str:
        if key in d:
            d[key]+=1
        else:
            d[key]=1
    sort_d=dict(sorted(d.items(),key=operator.itemgetter(1),reverse=True))
    for key, value in sort_d.items():
        print(key,' =',value)
str = input("please enter a string =")
most_frequent(str)
