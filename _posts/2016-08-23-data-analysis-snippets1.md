---
layout: post
title: Data Analysis Snippets-1
comments: true
---

![alt text](https://udemy-images.udemy.com/course/750x422/396876_cc92_7.jpg "Data Analysis with Python")

## This is ambitious!

Well ... as the world knows, Python is one of the coolest languages out there. 

And it is one of the most recommended languages particularly for data analysis. Mostly because of the kind of massive support given by python's existing libraries for this purpose. The power of python standard libraries is what we will see in this snippet.

## Some Background Noise ;-)

Life is all about data right now. So I chose to give myself a tough project. Every now and then, I want to record anything I find interesting in doing data analysis with python.

> Interestingly, I find Python as a friend in need, while I recommend Java as the Guru in all situations.

But as a matter of fact, given the kind of skills I have in either of these languages or in data analysis, this project is very ambitious. I still would like to give myself this challenge.

Here is the first interesting thing I want to talk about. There is nothing that I own here. I am just copying things from the book [Python for Data Analysis](http://www.cin.ufpe.br/~embat/Python%20for%20Data%20Analysis.pdf). But the point is, I am taking the most interesting thing in the initial 25 pages.

The first worked example in the text introduces about *1.USA.gov data from bit.ly*. This is what the introduction says:

> In 2011, URL shortening service bit.ly partnered with the United States government website usa.gov to provide a feed of anonymous data gathered from users who shorten links ending with .gov or .mil . As of this writing, in addition to providing a live feed, hourly snapshots are available as downloadable text files.

As said, this is true as of this book's writing. But I guess the data is not available now anymore where the author said it was. Instead, it is available in the author's [github repo](https://github.com/wesm/pydata-book/blob/master/ch02/usagov_bitly_data2012-03-16-1331923249.txt). The author, [Wes McKinney](https://github.com/wesm) shared all the worked out examples in the book in Jupyter Notebooks and shared them in [this repo](https://github.com/wesm/pydata-book), which makes it really interesting to learn from.

## Anyway, getting into the data now ...

The data specified here is in JSON format, but saved as a `.txt` file. There are a couple of ways I can load the data for my work in python. But the simplest way shown in the book is ...

```py
import json
path = 'ch02/usagov_bitly_data2012-03-16-1331923249.txt'
records = [json.loads(line) for line in open(path)]
```

Now if you just run `records[0]`, it will output the first line in the data in `dict` format.

```
{u'a': u'Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/535.11 (KHTML, like Gecko) Chrome/17.0.963.78 Safari/535.11',
u'al': u'en-US,en;q=0.8',
u'c': u'US',
u'cy': u'Danvers',
u'g': u'A6qOVH',
u'gr': u'MA',
u'h': u'wfLQtf',
u'hc': 1331822918,
u'hh': u'1.usa.gov',
u'l': u'orofrog',
u'll': [42.576698, -70.954903],
u'nk': 1,
u'r':
u'http://www.facebook.com/l/7AQEFzjSi/1.usa.gov/wfLQtf',
u't': 1331923247,
u'tz': u'America/New_York',
u'u': u'http://www.ncbi.nlm.nih.gov/pubmed/22415991'}
```

And the total number of records (lines in the data file) are 3560.

If you observe, one of the keys in this dict is `'tz'` which stands for `timezone`. You can extract all the values of this particular key in all the lines of the data and save it separately, like this.

```py
time_zones = [rec['tz'] for rec in records if 'tz' in rec]
```

And try `time_zones[:10]`, you will see the output as,

```
[u'America/New_York',
u'America/Denver',
u'America/New_York',
u'America/Sao_Paulo',
u'America/New_York',
u'America/New_York',
u'Europe/Warsaw',
u'',
u'',
u'']
```

Now, the author shows how to produce counts by time zones in different approaches.

## First Approach

### First step:

We are defining a new function `get_counts` that takes a `sequence` as an argument and counts what we want it to count.

```py
def get_counts(sequence):
  counts = {}
  for x in sequence:
  if x in counts:
    counts[x] += 1
  else:
    counts[x] = 1
  return counts
```

And the `sequence` in our example is `time_zones`, so ... running this line below gives us a dictionary with all the timezones as keys and their counts as values.

```
counts = get_counts(time_zones)
```

Try `print counts['America/New_York']` and the output is `1251`.

### Second step:
Now you need the top 10 timezones and their counts. We will define another function for this.

```py
def top_counts(count_dict, n=10):
  value_key_pairs = [(count, tz) for tz, count in count_dict.items()]
  value_key_pairs.sort()
  return value_key_pairs[-n:]
```

Our `count_dict` in this example is the dictionary of `counts`. Now, try `print top_counts(counts)` and the output looks like this.

```
[(33, u'America/Sao_Paulo'),
 (35, u'Europe/Madrid'),
 (36, u'Pacific/Honolulu'),
 (37, u'Asia/Tokyo'),
 (74, u'Europe/London'),
 (191, u'America/Denver'),
 (382, u'America/Los_Angeles'),
 (400, u'America/Chicago'),
 (521, u''),
 (1251, u'America/New_York')]
```

## Second Approach

All that we have done to achieve the last output can be done in 3 lines of code by using `Counter` method in `collections` library, which is one of the standard libraries of python.

```py
from collections import Counter
counts2 = Counter(time_zones)
counts2.most_common(10)
```

And that's it! It gives you the same output.

```
[(33, u'America/Sao_Paulo'),
 (35, u'Europe/Madrid'),
 (36, u'Pacific/Honolulu'),
 (37, u'Asia/Tokyo'),
 (74, u'Europe/London'),
 (191, u'America/Denver'),
 (382, u'America/Los_Angeles'),
 (400, u'America/Chicago'),
 (521, u''),
 (1251, u'America/New_York')]
```

I loved the way this difference made by using python standard libraries was taught. It really gives an insight into how I can make my job much faster and more effcient in doing data analysis with python.

Thanks for reading up to this line. Hope it made sense. I will come back with another snippet if I find anything interesting.

> **Enjoy Python!**
