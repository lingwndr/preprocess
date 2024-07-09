Usage
-----
Copy / paste this function
```python
def normalize(text):
  
  srcLine = ',?%1234567890;“”ﭘﺮﺯﻭﺻكىيﻬ٧ﺍﭙﺚﻖﯿﮎﺗﯼيﺴﻯﮥﺻﯾﺸﺿﻔﻐﻴﺞ٦ﻡےكﻩﺟﺜﻥﺰﻟﭻﻰﻣﻉﻳﺪﻤﺒ٤ﺫﺠﻲﺳﻓﺭﺨﮏﺕﻧﺵﮑ١ﮔﻗ٢ﺘﻱﻭﮯ٥ٱﻫﺩ٨ﻏﻦﻠﺺﺼﭘﺖﺏﻕﺲﺷۀﻎﻝﭽﻮﻑﺶﻨﺮﮕﮐﺣ٩٠٣ةﻍﺝﻒﭼﮓﺹﻌﯽﺛﻄڪﺬﻃﻢﻋﺑﺧﻂﺤﺥﻊﺁﻜﻞﺦﻛﺎﺯﻘﺱﻪہﺐى'
  trgLine = '،؟٪۱۲۳۴۵۶۷۸۹۰؛""پرزوصکییه۷اپثقیکتییسیهصیشضفغیج۶میکهجثنزلچیمعیدمب۴ذجیسفرخکتنشک۱گق۲تیویهاهد۸غنلصصپتبقسشهغلچوفشنرگکح۹۰۳هغجفچگصعیثطکذطمعبخطحخعآکلخکازقسههبی'

  repl = str.maketrans(srcLine, trgLine)
  repl[172] = 8204 # converting Microsoft Word ZWNJ to the unicode standard ZWNJ
  return text.translate(repl)
```

```python
>>> normalize("1 کتاب خریدم, ديدي?")
'۱ کتاب خریدم، دیدی؟'
```
