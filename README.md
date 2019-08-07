# Fullcalendar Ruby Gem

This gem is a fork of [fullcalendar](https://github.com/mkhairi/fullcalendar) updating it to last version of FullCalendar (4.2)

This gem just includes [fullcalendar](https://fullcalendar.io/) and [scheduler](https://fullcalendar.io/scheduler/) as an asset in rails applications or other ruby frameworks
[Fullcaledar-scheduler](https://fullcalendar.io/scheduler/) is not free for commercial use, so make sure you have a valid [license](https://fullcalendar.io/scheduler/license/) to use scheduler.


## Installation

Fullcalendar JavaScript depends on jQuery and moment js. If you're using Rails 5.1+, add the jquery-rails gem to your Gemfile:

```ruby
gem 'jquery-rails'
gem 'momentjs-rails'
```

Add this line to your application's Gemfile:

```ruby
gem 'rails-fullcalendar'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install rails-fullcalendar


## Install generator

### command
```ruby
rails g fullcalendar:install 
```

this generator will: 
  -  1. append ```//= require calendar ``` add `app/assets/javascripts/application.js`
  -  2. append ```*= require calendar ``` add `app/assets/stylesheets/application.css`
  -  3. create calendar.js  in ```app/assets/javascripts/```
  -  4. create calendar.scss in  ```app/assets/stylesheets/```

## Manual install

### JavaScripts

Include the JavaScript in your `app/assets/javascripts/application.js`:
```
//= require jquery
//= require calendar

```
create new file `app/assets/javascripts/calendar.js`
```
//Core component
//= require fullcalendar
// optional locale
//= require fullcalendar/locale/ms

//Optional addon scheduler
//= require fullcalendar/scheduler

```

### Stylesheets 
Include the stylesheet in your `app/assets/stylesheets/application.css`:
```
*= require calendar
```

or if you using scss

Include the stylesheet in your `app/assets/stylesheets/application.scss`:
```scss
@import 'calendar';
```

Create new file `app/assets/stylesheets/calendar.scss`
```scss
@import 'fullcalendar';
```

### Initialization 
Where needed in your JavaScripts, initialize your fullcalendar:

```js
$(document).ready(function() {
  var calendarEl = document.getElementById('calendar');
  new (FullCalendar.Calendar)(calendarEl);
});
```

## Usage
see fullcalendar documentations [here](https://fullcalendar.io/docs)

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).  
Fullcalendar and Scheduler, which makes up the majority of this gem, has its own, separate licensing  agreement.   
- Fullcalendar [Read license](https://github.com/fullcalendar/fullcalendar/blob/master/LICENSE.txt)    
- Scheduler [Read license](https://github.com/fullcalendar/fullcalendar-scheduler/blob/master/LICENSE.md)  
