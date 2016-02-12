# Forms & HTML

[![Build Status](https://travis-ci.org/Satsume/html.svg?branch=master)](https://travis-ci.org/Satsume/html)
[![Total Downloads](https://poser.pugx.org/jaapmoolenaar.nl/html/downloads)](https://packagist.org/packages/jaapmoolenaar.nl/html)
[![Latest Stable Version](https://poser.pugx.org/jaapmoolenaar.nl/html/v/stable)](https://packagist.org/packages/jaapmoolenaar.nl/html)
[![Latest Unstable Version](https://poser.pugx.org/jaapmoolenaar.nl/html/v/unstable)](https://packagist.org/packages/jaapmoolenaar.nl/html)
[![License](https://poser.pugx.org/jaapmoolenaar.nl/html/license)](https://packagist.org/packages/jaapmoolenaar.nl/html)

Official documentation for Forms & Html for The Laravel Framework can be found at the [LaravelCollective](http://laravelcollective.com) website.

# Additions

Labels are now allowed to contain HTML if the fourth parameter is set to true.

```php
Form::label('email', '<i class="fa fa-envelope"></i> E-mail Address', [], true)
```

Will result in
```html
<label for="email"><i class="fa fa-envelope"></i> E-mail Address</label>
```

This is useful for wrapping checkboxes in a label:
```php
$checkbox = Form::checkbox('remember');
Form::label('remember', $checkbox.' Remember me', [], true)
```

Will result in
```html
<label for="remember"><input type="checkbox" name="remember"> Remember me</label>
```