# Dynamic-Localization-with-Laravel
Hello everyone! this project is based on Dynamic localization with Laravel 
<br>
for starting localizatoin we need to install :
<br>
1- Laravel fresh project  (https://laravel.com/docs/8.x)
<br>
2- Localization package (https://github.com/mcamara/laravel-localization)
<br>

3- Xampp server
<br>

4- Code editor
<br>

after installing and setup of the project we are going to setup database and migration:
<br>
DATABASE NAME: codeconf
<br>
ROOT: null
<br>
Password: null
<br>
in cmd run this code
<br>
php artisan migrate
<br>

after that add some data in table (posts)
<br>
//remember you have to uncomment the languages from config/laravellocalization.php
<br>


add this peice of code at the top of your controller 
<br>
<span>
     
      private $language;
      public function __construct()
        {
        	$this->language = \LaravelLocalization::getCurrentLocale() == 'en' ? 'english' : (\LaravelLocalization::getCurrentLocale() == 'fa' ? 'dari' : 'pashto');
        }
 </span>
        
        <br>
 according to your langs add anchor tags
 <br>
 
 <a href="{{LaravelLocalization::getLocalizedURL('en') }}" >English </a>
 <br>
 
 <a href="{{LaravelLocalization::getLocalizedURL('en') }}" >دری </a>
 <br>
 <a href="{{LaravelLocalization::getLocalizedURL('en') }}" >پښتو </a>
 
 
 
 

