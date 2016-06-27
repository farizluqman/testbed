# Damn Stupid Simple PHP Framework

[![Version](https://badge.fury.io/gh/damnstupidsimple%2Fframework.svg)](https://badge.fury.io/gh/damnstupidsimple%2Fframework)
[![Build](https://api.travis-ci.org/damnstupidsimple/framework.svg)](https://travis-ci.org/damnstupidsimple/framework)
[![License](https://img.shields.io/:license-mit-blue.svg)](https://github.com/damnstupidsimple/framework/blob/master/LICENSE)
![Made In](https://img.shields.io/badge/made%20in-Malaysia-red.svg)

Damn Stupid Simple is a micro framework built for lazy developers. Suitable for those who used to develop vanilla projects, while following today's set of standard. The core is very small in size, yet it contains most of the functions required to rapidly start developing a project. The name itself is obvious.

> New programmers have to take extra effort to learn 
> everything about modern PHP frameworks like Laravel and Symphony. Most 
> of the time were spent on documentations rather than the actual codes.
> This leads to the development of Damn Stupid Simple, as the surface of
> every terminologies, and the entry level to modern day needs. 
> Damn Stupid Simple is hybrid, and it's all you need to start grasping
> modern framework styles. It is everything you need to run from small to large-scale projects.

Latest Version
----
Release 0.1.0

### Table of Contents
| No | Title                                              |
|----|----------------------------------------------------|
| 1  | [Why Damn Stupid Simple?](#why-damn-stupid-simple) |
| 2  | [Technical Features](#technical-features)          |
| 3  | [How to Install](#installation)                    |
| 4  | [Basic Application](#basic-application)            |
| 5  | [API Documentation](#api-documentation)            |


Why Damn Stupid Simple
----
  - No nonsense
  - Follow your own style
  - Extremely extensible
  - Small in size
  - Lightning fast (<20 ms)

[[back to top]](#table-of-contents)

Technical Features
----
  - **Lazy Routing** - Route urls according to file names. Your /home will be redirected to home.php and so on.
  - **Simple Templating Process** - Copy and paste any templates you downloaded to the root directory, and viola, it's up and ready. However, you can still manage template them however that suits your likings.
  - **Integrated with Composer** - Download thousands of packages available straight to your project.
  - **Integrated with Eloquent ORM** - Manage database records with no hassles. 
  - **Dependency Injection** - Minimize coupling and dependant on a single project. And provides easy access to objects and variables.
  - **Out-of-the-Box Error Handler** - We integrated the framework with [Whoops](https://filp.github.io/whoops/), error handler in a less painful way.

[[back to top]](#table-of-contents)

Installation
----
Damn Stupid Simple requires PHP >= 5.4 to run.

##### 1. Install via Composer; or

If you do not have Composer installed, please follow [this link](https://getcomposer.org/doc/00-intro.md#using-the-installer) for Windows, or [this link](https://getcomposer.org/doc/00-intro.md#downloading-the-composer-executable) for Mac Os X and Linux.

As soon as you have installed the Composer already, type this on the Command Prompt (or Terminal)
```sh
$ composer create-project damnstupidsimple/framework myproject
```

##### 2. Install via Zip/Tarball File:
Simply go to the [Releases page](https://github.com/damnstupidsimple/framework/releases) to download .zip or .tar file for Damn Stupid Simple framework.

[[back to top]](#table-of-contents)

Basic Application
----
```php
<?php
// All of the core classes are in this namespace
namespace Core;

// Define the root directory
define('DSS_PATH', __DIR__ . '/');

// Require Composer's fantastic autoloader to load 3rd party packages
require_once(DSS_PATH.'app/autoloader.php');

// Lazy routing
Router::get('/(:any)', function() {
	Viewer::file('home.php');
});

// Dispatch the router and done
Router::dispatch();
?>
```

[[back to top]](#table-of-contents)

API Documentation
----
Table of contents
| No | Class         | Contents |
|----|---------------|----------|
| 1  | Core\Router   | <ul><li>item1</li><li>item2</li></ul> |
| 2  | Core\Viewer   |          |
| 3  | Core\App      |          |
| 4  | Core\Sharer   |          |
| 5  | Core\Database |          |
| 6  | Core\Cache    |          |
| 7  | Core\Debugger |          |

[[back to top]](#table-of-contents)

Development
----
Want to contribute? Great! Please do not hesitate to contribute to the framework development.

[[back to top]](#table-of-contents)

License
----
MIT

[[back to top]](#table-of-contents)

Todo
----
This is a work in progress. The README.md will be expanded from time to time.

[[back to top]](#table-of-contents)
