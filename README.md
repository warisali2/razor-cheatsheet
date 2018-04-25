# Razor Cheatsheet
A simple razor cheatsheet

## Table of Contents
* [Introduction](#introduction)
* [Razor Code Block](#razor-code-block)
* [Render HTML](#render-html)

## Introduction
Razor is a markup syntax for embedding server-based code into webpages. The Razor syntax consists of Razor markup, C#, and HTML. Files containing Razor generally have a .cshtml file extension.

## Razor Code Block
A razor block consists of 
```razor
@{
  //Your code here
}
```
You can use any C# code in razor block.

## Render HTML
Anything in Razor Block that is not C#, will be rendered as HTML. For exmaple
```razor
@{
  for(int i = 0; i < 3; i++)
    <span>Hello</span>
}
```
Will be rendered as `Hello Hello Hello`
