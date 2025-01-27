#### Описание:  

Регулярное выражение по поиску валидного url.  

#### Набор данных для проверки:

2025-01-20 10:26:04.792 DEBUG [,5c6ec2bdb2419d7b,5c6ec2bdb2419d7b] 17576 --- [nio-8080-exec-3] o.s.web.client.RestTemplate              : Response 400 BAD_REQUEST  
***2025-01-20 10:26:04.808 ERROR*** [,5c6ec2bdb2419d7b,5c6ec2bdb2419d7b] 17576 --- [nio-8080-exec-3] s.t.s.service.impl.PaymentServiceImpl    : Got an error from exchange service: 400 Bad Request: [{
    "disclaimer": "https://www.cbr-xml-daily.ru/#terms",
    "date": "2024-09-07",
    "timestamp": 1725656400,
    "base": "RUB",
    "rates": {
        "AUD": 0.0165572,
        "AZN": 0.01... (1342 bytes)]  
2025-01-20 10:26:04.816 DEBUG [,5c6ec2bdb2419d7b,5c6ec2bdb2419d7b] 17576 --- [nio-8080-exec-3] .m.m.a.ExceptionHandlerExceptionResolver : Using @ExceptionHandler some.testme.server.config

#### Регулярное выражение:
```
(\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}.+) (ERROR|INFO|WARNING)
```
