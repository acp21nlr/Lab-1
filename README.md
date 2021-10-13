# Lab-1
movie body count
import urllib.request
urllib.request.urlretrieve('https://github.com/sjmgarnier/R-vs-Python/archive/master.zip', './master.zip')
import zipfile
zip = zipfile.ZipFile('./master.zip', 'r')
for name in zip.namelist():
    zip.extract(name, '.')
    import pandas as pd # import the pandas library into a namespace called pd
film_deaths = pd.read_csv('./R-vs-Python-master/Deadliest movies scrape/code/film-death-counts-Python.csv')
