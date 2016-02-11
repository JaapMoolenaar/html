# Forms & HTML

[![Build Status](https://travis-ci.org/LaravelCollective/html.svg)](https://travis-ci.org/LaravelCollective/html)
[![Total Downloads](https://poser.pugx.org/LaravelCollective/html/downloads)](https://packagist.org/packages/laravelcollective/html)
[![Latest Stable Version](https://poser.pugx.org/LaravelCollective/html/v/stable.svg)](https://packagist.org/packages/laravelcollective/html)
[![Latest Unstable Version](https://poser.pugx.org/LaravelCollective/html/v/unstable.svg)](https://packagist.org/packages/laravelcollective/html)
[![License](https://poser.pugx.org/LaravelCollective/html/license.svg)](https://packagist.org/packages/laravelcollective/html)

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