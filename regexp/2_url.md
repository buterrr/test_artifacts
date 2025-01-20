#### Описание:

Регулярное выражение по поиску валидного url.

#### Набор данных для проверки:

* ***https://regex101.com/***  
* ***http://regex101.com/***  
hts://regex101.com/  
https://regex101  
https://.com/  
* ***https://regex101.sedf.com***  
regex101@mail.com/  
* ***http://example.org/path?param=value***  

#### Регулярное выражение:

https?:\/\/[a-zA-Z0-9.-]+\.[a-zA-z]{2,}(?:\/[^\s]*)?
