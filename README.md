# Python telegram bot

## Функциональность и используемые API

Бот принимает на вход текстовый запрос с указанием даты и города и вовзвращает температуру (дневную и ночную) в указанную дату, погоду, картинку соответсвующую этой погоде и стихотворение.

Бот использует следующие API:
1. API Telegrama для обработки текстовых запросов и отправки текста и картинок.
2. API Яндекс Погоды для выдачи прогноза наиболее релевантному к заданному запросу.
3. API Bing картинок для нахождения картинок, наиболее релевантных заданному городу из запроса, и соответсвующей погоды на выбранную дату.

Также бот использует стихотворения Марины Цветаевой, релевантные соответсвующей погоде на заданную дату, с сайта lib.ru

## Обрабатываемые запросы
Бот принимает запросы на английском языке и обрабатывает запросы следующего вида:  
* *Madrid*  
* *Weather in Barcelona*  
* *Weather in San Francisco tomorrow*  
* *Kazan Thursday*  
* *Weather in New York in three days*  

Также бот понимает команды:
* */start*
* */help*

## Принцип работы
Бот принимает на вход строку, внутри которой распознает город при помощи словаря городов, предоставляемого API Яндекс Погоды, а также пытается распознать дату, на которую нужно сделать прогноз. При неудачном распознавании города бот возвращает строку *City not found*, а при неудачном распознавании даты, выводится погода за сегодня.   
По распознанным городу и погоде бот ищет и выдает картинку этой погоды в соответсвующем городе при помощи API Bing картинок, а также выводит стихотворение, соответсвующее этой погоде.
  
  
