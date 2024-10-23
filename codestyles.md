# HTML Coding Standards
> Source: [Bootstrap Code Guidelines](https://codeguide.bootcss.com/) <br/>
> Source: [Baidu EFE Coding Standards](https://github.com/ecomfe/spec) <br/>

<br/>

**Table of Contents**

1. [Attribute Order](#1-attribute-order)
2. [Class Naming](#2-class-naming)
3. [ID Naming](#3-id-naming)
4. [Name Naming](#4-name-naming)

## 1. Attribute Order
HTML attributes should be arranged in the following order to ensure code readability:
* `class`
* `id`, `name`
* `data-*`
* `src`, `for`, `type`, `href`, `value`
* `title`, `alt`
* `role`, `aria-*`

`class` should come first as it identifies highly reusable components.

`id` should be used cautiously (e.g., for bookmarks within a page) and thus comes second.

Example:
```html
<a class="..." id="..." data-toggle="modal" href="#">
  Example link
</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```

<br/>

## 2. Class Naming
* `class` names must use all lowercase letters, with words separated by hyphens (`-`);
* `class` names must represent the content or functionality of the respective module or component, and should not be named based on stylistic information;
* Avoid excessively arbitrary abbreviations. `.btn` represents `button`, but `.s` does not convey any meaning;
* Prefix new classes based on the closest parent class or base class.

Example:
```html
<!-- good -->
<div class="sidebar"></div>

<!-- bad -->
<div class="left"></div>
```
For common naming conventions, refer to [AlloyTeam](http://www.alloyteam.com/2011/10/css-on-team-naming/).

<br/>

## 3. ID Naming
* Element `id` must be unique within the page;
* It is recommended that `id` names use all lowercase letters, with words separated by hyphens (`-`). Consistency must be maintained within the same project.
* `id` and `class` names should be as short as possible while avoiding conflicts and providing clear description.

Example:
```html
<!-- good -->
<div id="nav"></div>
<!-- bad -->
<div id="navigation"></div>

<!-- good -->
<p class="comment"></p>
<!-- bad -->
<p class="com"></p>

<!-- good -->
<span class="author"></span>
<!-- bad -->
<span class="red"></span>
```

<br/>

## 4. Name Naming
* On the same page, avoid using the same `name` and `id`.
* `name` should generally follow the naming conventions of fields in the backend model.
  * For example, Java uses camelCase, while Python uses underscores (`_`) to connect two lowercase words.

Explanation:

IE browsers can confuse elements' `id` and `name` attributes, and `document.getElementById` might retrieve an unexpected element. Therefore, it is crucial to be cautious when naming elements' `id` and `name` attributes.

A good practice is to use different naming conventions for `id` and `name`.

Example:
```html
<input name="foo">
<div id="foo"></div>
<script>
// IE6 will display INPUT
alert(document.getElementById('foo').tagName);
</script>
```

<br/>
<br/>
