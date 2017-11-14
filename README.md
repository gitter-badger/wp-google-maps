# WP Google Maps

[![Waffle.io - Columns and their card count](https://badge.waffle.io/clubdeuce/wp-google-maps.svg?columns=all)](https://waffle.io/clubdeuce/wp-google-maps)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/clubdeuce/wp-google-maps/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/clubdeuce/wp-google-maps/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/clubdeuce/wp-google-maps/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/clubdeuce/wp-google-maps/?branch=master)
[![Build Status](https://travis-ci.org/clubdeuce/wp-google-maps.svg?branch=master)](https://travis-ci.org/clubdeuce/wp-google-maps)

A Google Maps library for WordPress.


## Installation

This project can be installed via [Composer[(https://getcomposer.org):

`composer require clubdeuce\wp-google-maps`

Simply include `autoload.php` from your `vendor` directory and the library will be included.


## Usage

A simple example:

```

use Clubdeuce\WPGoogleMaps\Google_Maps;
use Clubdeuce\WPGoogleMaps\Map;
use Clubdeuce\WPGoogleMaps\Marker;
use Clubdeuce\WPGoogleMaps\Map_View;

Google_Maps::register_script_condition( 'is_single' );
$map = new Map();
$map->add_marker( new Marker( array( 'address' => '1600 Amphitheatre Parkway, Mountain View, CA 94043') ) );
$view = new Map_View( $map );
$view->the_map();
```