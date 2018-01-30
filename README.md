# DATA
What I'm trying to do is put all my data on Github so whenever someone is running a script of mine they don't have to download the files themselve, they can simply pull the data from a URL to this repository making my code much more replicable and hopefully saving myself some headaches in the future. 


NOTE: IMPORTANT. Make sure whenever you're copying the url that its the RAW url. You can find it by clicking the RAW button next to BLAME and HISTORY and then copying that url.

``` R
    library(RCurl)
    library(foreign)
    url <- "https://raw.githubusercontent.com/JPMOS/Open_Data/master/titanic.csv"
    titanic.data <- getURL(url)                
    titanic.data <- read.csv(textConnection(titanic.data))

head(titanic.data)
```

Below is some code for python you can use as a template. 

``` Python
import requests
url = "https://raw.githubusercontent.com/JPMOS/Open_Data/master/data.txt"
r = requests.get(url)
text = r.text
print(text)
```
