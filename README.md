# Vue-event-calendar
* Use v-calendar to display calendar (CDN)
* Use JavaScript EventListener to listen to selected date on calendar
* Pass selected date from Javascript to PHP and check date from JSON file

### CDN V-calendar
Source: https://vcalendar.io/guide/#cdn
```
<html>
  <head>
    <meta charset='utf-8'>
    <meta name='viewport' content='width=device-width, initial-scale=1, shrink-to-fit=no'>
    <meta http-equiv='x-ua-compatible' content='ie=edge'>
    <!-- IMPORTANT: No CSS link needed as of v1 Beta (@next) - It's all inlined -->
    <!-- Pre v1.0.0 versions need the minified css -->
    <!-- <link rel='stylesheet' href='https://unpkg.com/v-calendar/lib/v-calendar.min.css'> -->
  </head>
  <body>
    <div id='app'>
      <v-calendar></v-calendar>
      <v-date-picker :mode='mode' v-model='selectedDate' />
    </div>

    <!-- 1. Link Vue Javascript -->
    <script src='https://unpkg.com/vue/dist/vue.js'></script>

    <!-- 2. Link VCalendar Javascript (Plugin automatically installed) -->
    <!-- @next v1 Beta  -->
    <script src='https://unpkg.com/v-calendar@next'></script>
    <!-- Latest stable (Right now, this is very different from the v1 Beta)-->
    <!-- <script src='https://unpkg.com/v-calendar'></script> -->
    <!-- Hardcoded version -->
    <!-- <script src='https://unpkg.com/v-calendar@1.0.0-beta.14/lib/v-calendar.umd.min.js'></script> -->

    <!--3. Create the Vue instance-->
    <script>
      new Vue({
        el: '#app',
        data: {
          // Data used by the date picker
          mode: 'single',
          selectedDate: null,
        }
      })
    </script>
  </body>
</html>
```


### Disabled past date (grey date) until current date (today)
#### Available dates ':available-dates='{ start: new Date(), end: null }'
```
<v-calendar :attributes='attrs' :available-dates='{ start: new Date(), end: null }'>
```

### Reference:
##### V-calendar
https://vcalendar.io/guide/#collections
https://vcalendar-legacy.netlify.com/popovers.html#labels
https://vuejsfeed.com/blog/v-calendar-a-clean-and-lightweight-calendar-plugin-for-vue-js 
+ customer v-calendar https://vcalendar.netlify.com/
https://medium.com/@nathanreyes/introducing-v-calendar-a-vue-js-plugin-for-attributed-calendars-2caaceeafde0
https://dbrekalo.github.io/vue-date-pick/examples.html#calendar-widget

##### Parse JSON with PHP
https://www.youtube.com/watch?v=Ua8oqm_HBSY

##### Encode | Decode JSON
https://www.tutorialrepublic.com/php-tutorial/php-json-parsing.php

##### Pass JavaScript value to PHP via AJAX
https://www.w3schools.com/php/php_ajax_php.asp

##### Check a specific word contains in String in PHP
https://www.tutorialrepublic.com/faq/how-to-check-if-a-string-contains-a-specific-word-in-php.php

##### JavaScript session
https://www.w3schools.com/jsref/prop_win_sessionstorage.asp
https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage
https://www.splessons.com/lesson/javascript-session/

##### PHP session
https://www.tutorialspoint.com/php/php_sessions.htm

#### JavaScript Fetch API
https://hospodarets.com/fetch_in_action
