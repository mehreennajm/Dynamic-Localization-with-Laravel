# Dynamic-Localization-with-Laravel
Hello everyone! this project is based on Dynamic localization with Laravel 
for starting localizatoin we need to install :
1- Laravel fresh project  (https://laravel.com/docs/8.x)
2- Localization package (https://github.com/mcamara/laravel-localization)
3- Xampp server
4- Code editor

after installing and setup of the project we are going to setup database and migration
DATABASE NAME: codeconf
ROOT: null
Password: null
in cmd run this code
php artisan migrate

after that add some data in table (posts) 
//remember you have to uncomment the languages from config/laravellocalization.php


add this peice of code at the top of your controller 
      private $language;
      public function __construct()
        {
        	$this->language = \LaravelLocalization::getCurrentLocale() == 'en' ? 'english' : (\LaravelLocalization::getCurrentLocale() == 'fa' ? 'dari' : 'pashto');
        }
        
 according to your langs add anchor tags
 <a href="{{LaravelLocalization::getLocalizedURL('en') }}" >English </a>
 <a href="{{LaravelLocalization::getLocalizedURL('en') }}" >دری </a>
 <a href="{{LaravelLocalization::getLocalizedURL('en') }}" >پښتو </a>
 
 
 

