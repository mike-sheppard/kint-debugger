# Kint Debugger

Dump variables and traces in an organized and interactive display. Integrates seamlessly with Debug Bar.

**Kint Debugger** is a simple wrapper for [Kint](https://github.com/raveren/kint), a debugging tool to output information about variables and traces in a styled, collapsible format that makes understanding deep arrays and objects easier.

## Basic Usage

```php
d($var);
```

```php
global $post;
d($post);
```

```php
global $post;
$term_list = wp_get_post_terms($post->ID, 'my_taxonomy', ['fields' => 'all']);
d($term_list);
ddd($term_list); // debug + die()
```

#### Kint Debugger also provides some helper functions for dumping variables that are frequently needed.

* `dump_wp_query()`
* `dump_wp()`
* `dump_post()`

`<?php dump_post(); ?>`

`<?php add_action( 'wp_head', 'dump_post' ); ?>`


## Changelog

#### 1.0.0

* Fork updated [kint-debugger](https://github.com/DuckDivers/kint-debugger) with php 7.4 support
* Rip out most of it, use composer to load latest version of [Kint](https://github.com/kint-php/kint)
