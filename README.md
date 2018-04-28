# Razor Cheatsheet
A simple razor cheatsheet

## Table of Contents
* [Introduction](#introduction)
* [Razor Code Block](#razor-code-block)
* [Render HTML](#render-html)
* [Use Variables in HTML](#use-variables-in-html)
* [Section](#section)

## Introduction
Razor is a markup syntax for embedding server-based code into webpages. The Razor syntax consists of Razor markup, C#, and HTML. Files containing Razor generally have a .cshtml file extension.

## Razor Code Block
A razor block consists of 

```
@{
  //Your code here
}
```

You can use any C# code in razor block.

## Render HTML
Anything in Razor Block that is not C#, will be rendered as HTML. For exmaple

```c#
@{
  for(int i = 0; i < 3; i++)
    <span>Hello</span>
}
```

Will be rendered in HTML as 

```html
<span>Hello</span>
<span>Hello</span>
<span>Hello</span>
```

## Use Variables in HTML
We can use C# variables in our HTML code by prefixing its name with `@`

```c#
@{
  var myGreetings = "Hello World";
}

<p>myGreetings: @myGreetings</p>
```

It will be rendered as `myGreetings: Hello World`

**Note** To escape `@` in Razor Markup, use a second `@` with symbol

```c#
<p>@@myvar</p>
```

It will be rendered as 

```html
<p>@myVar</p>
```

## Section
We can define a section that can be used in a layout as follows:
```html
@section section_name
{
  <h1>Hello Section</h1>
}
```
