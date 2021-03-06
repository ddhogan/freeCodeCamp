# localeTitle: undefined
React Router для начинающих

# Монтаж

React Router был разбит на три пакета: `react-router` , `react-router-dom` и `react-router-native` .

Вам почти никогда не придется устанавливать реактивный маршрутизатор напрямую. Этот пакет предоставляет основные компоненты и функции маршрутизации для приложений React Router. Другие два предоставляют специфические для среды (браузеры и реагирующие на) компоненты, но оба они также реэкспортируют все экспортные реакции-маршрутизатора.

Мы создаем веб-сайт (что-то, что будет запускаться в браузерах), поэтому мы установим response-router-dom.

`npm install --save react-router-dom`

# Маршрутизатор

При запуске нового проекта вам необходимо определить, какой тип маршрутизатора использовать. Для проектов на базе браузера есть а также компоненты. `<BrowserRouter>` следует использовать, когда у вас есть сервер, который будет обрабатывать динамические запросы (знает, как реагировать на любой возможный URI), в то время как должен использоваться для статических веб-сайтов (где сервер может отвечать только на запросы файлов, о которых он знает).

Обычно рекомендуется использовать `<BrowserRouter>` , но если ваш сайт будет размещен на сервере, который обслуживает только статические файлы, то `<HashRouter>` является хорошим решением.

Для нашего проекта мы предположим, что веб-сайт будет поддерживаться динамическим сервером, поэтому нашим компонентом маршрутизатора является `<BrowserRouter>` .

# Импортный отчет

```javascript
import { BrowserRouter as Router, Switch, Route, Link } from 'react-router-dom'; 
```

## IndexRoute и ссылки

Теперь давайте добавим навигацию, чтобы получить нас между страницами.

Для этого мы будем использовать компонент `<Link>` . `<Link>` похожа на использование тега привязки html.

Из документов:

Основной способ разрешить пользователям перемещаться по вашему приложению.  сделает полностью доступный тег привязки с соответствующим href. Для этого сначала создадим компонент Nav. Наш компонент Nav будет содержать компоненты `<Link>` и будет выглядеть так:

```javascript
const Nav = () => ( 
  <div> 
    <Link to='/'>Home</Link>&nbsp; 
    <Link to='/address'>Address</Link> 
  </div> 
 ) 

```