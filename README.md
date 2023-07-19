## What are Laravel Stub?
In Laravel, stubs are templates used for generating code files. When you create a new class, controller, migration, or other type of file in Laravel using the php artisan command-line tool, Laravel generates a new file based on a stub template.

The Laravel framework comes with a set of default stubs for generating common types of files. These stubs are stored in the resources/stubs directory of your Laravel application and can be customized to fit your specific project needs.

So, Stub are nothing, these are predefined core templates for classes. These files provide a predefined skeleton for controller, model etc.

Example:
--<?php namespace {{ namespace }}; use {{ rootNamespace }}Http\Controllers\Controller; use Illuminate\Http\Request; class {{ class }} extends Controller { // } 

- {{ namespace }}, {{ rootNamespace }}, {{ class }} These are placeholders which will replaces when we pass class name, namespace into artisan command to generate controllers.


## When we run the command

$ php artisan make:controller TestController

Controller stub file will execute, replace all placeholders in a dynamic way and generate controller.

## Laravel Stub Publish

To work with laravel stub files, first we need to publish it. When we publish stub then all files of stub will be located within a stubs directory in the root of your application.

By default you will not see this folder (stubs) into application root.

Publish Stubs

$ php artisan stub:publish
