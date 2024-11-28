# Sofia-Schedule-grabber
Sofia's Public transport scedule web crawler using python.

> [!NOTE]
> We are using the offical [sofiatraffic](https://www.sofiatraffic.bg/bg/public-transport) web portal.
> And a web Crawler

# Dependencies:
- Selenium (ChromeDriver)
- chromium-browser
- chromium-chromedriver
- Python3
- Pip3

# Installing
> [!WARNING]
> It is recomended to use Linux, because it was build for linux

## Selenium
```
  pip install selenium
```
## For linux (Chromium for web-crawler):
- chromium-browser
```
sudo apt install chromium-browser
```
- chromium-chromedriver
```
sudo apt install chromium-chromedriver
```
## For Windows (Chromium for web-crawler):
- Install chromuim drivers from [here](https://download-chromium.appspot.com/dl/Win_x64?type=snapshots)
- In the python file replace this line:
```
service = Service("/usr/bin/chromedriver")      # !!!Please Change this unless you are in linux
```
With this:
```
service = Service("")      # !!!Please Change this unless you are in linux
```
- in `Command Promt` with elevated privilages install Selemium (Section Installing)

# Configuring Bus, Number, Stop.
## First we have the bus stop:
```
BUS = ""
```
We can configure it by just putting the bus number we want.
Example of this line is:
```
BUS = "8"
```

## Next we have the (Bus)Stop Number
```
STOP = ""
```
We can cofigure it by going to the offical Sofia-Transport site: [sofiatraffic.bg](https://www.sofiatraffic.bg/bg/public-transport)
and selecting our stop. Each stop has an unique number. For example: 	`НДК (1136)`, Where `1136` is the unique number.
Example of this line is:
```
STOP = "1136"
```

## Finally we have the Nick (Or the Bus stop name)
```
NICK = ""
```
We can configure this by getting the name of the stop. For example `НДК (1136)`, And the name is `НДК`. Please use **UPPER CASE** and **SINGLE WORDS** for this. The web crawler otherwise will not recognise the stop.
For Example we have stop: `ПЛ. ЖУРНАЛИСТ (1273)` We need to type **ONLY** "ЖУРНАЛИСТ" (By the way you can add all but only if there are more stops with the same name so if there are 5 "НДЛ" please put the name followed by space and after that in brackets the unique code so: `НДК (1136)`)
Example of this line is:
```
NICK = "НДК"
NICK = "ЖУРНАЛИСТ"
NICK = "НДК (1136)"
```

# License
- From [https://www.chromium.org](https://www.chromium.org/Home/)

Except as otherwise [noted](https://developers.google.com/site-policies.html#restrictions), the content of this page is licensed under a [Creative Commons Attribution 2.5 license](https://creativecommons.org/licenses/by/2.5/), and examples are licensed under the [BSD License](https://chromium.googlesource.com/chromium/src/+/HEAD/LICENSE).
