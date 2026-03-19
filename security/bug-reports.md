#Идентификатор ошибки 1#
*Environment:* 
Win 11 Pro Chrome 146
*Severity:* 
Critical
*Title: 
Главная страница CodeLibs.ru уязвима к clickjacking, при загрузке сайта в <iframe> на стороннем домене, так как отсутствуют ограничения через X-Frame-Options и/или Content-Security-Policy: frame-ancestors.
*Precondition:* 
1. Страница https://www.CodeLibs.ru/ открыта в браузере
2. Открыта DevTools (F12)
*Steps:*
1. Открыть вкладку Network в DevTools
2. Кликнуть на запрос к truck1.eu
3. Открыть вкладку Headers
*Expected Result:*
Браузер должен блокировать загрузку страницы в iframe и отображать пустой фрейм. В Response Headers должен присутствовать один из заголовков: X-Frame-Options: SAMEORIGIN  или  Content-Security-Policy: frame-ancestors 'self'

*Actual Result:*
Страница https://www.CodeLibs успешно загружается внутри <iframe>. Заголовок X-Frame-Options и директива CSP frame-ancestors в ответе сервера отсутствуют.
