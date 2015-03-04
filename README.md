# Answers: Bitmaker's FED - CSS Selectors Assignment

## Assignment Overview

1. [Selectors](#selectors)
2. [The Cascade](#the-cascade)
3. [Specificity](#specificity)
4. [Combining Selectors](#combining-selectors)
5. [Pseudo-class selectors](#pseudo-class-selectors)


## Selectors

There are three types of basic selectors:


### Tag selectors

Tag selectors select all elements on a page of a particular type. This is the broadest selector since it will match all elements of a particular type.

If we want to apply styles to all paragraphs in the entire document, we would use a tag selector.

```
p {
  font-size: 20px;
}
```


### Class selectors

Class selectors select all elements on the page with a given class, regardless of its type. This is much more specific than a tag selector since by default none of the elements have classes applied, and we would add them in our HTML to the ones that should have the styles. We will use class selectors most of the time when styling our documents.

If we want to apply styles to all of the elements with class "highlight", we would use a class selector.

```
.highlight {
  background-color: yellow;
}
```


### ID selectors

ID selectors select the one element on the page that has a particular ID. This is the most specific type of selector because IDs are unique in the document so an ID selector will select at most one element. We'll avoid using this type of selector for styling since it's overly specific most of the time and makes overriding styles very difficult.

If we want to apply styles to all of the elements with ID "container", we would use an ID selector.

```
#container {
  width: 80%;
}
```


## The Cascade

The first C in CSS stands for "Cascading". Cascade, in the context of CSS, allows style rules to be built up incrementally or overridden by other sets of rules that target the same elements through their selectors. The cascade manifests itself in a few ways.

1. Rules that come later inherit from or override previous rules that select the same element
2. Properties that come later within the same rule will override identical properties that come earlier


## Specificity

The specificity of the selectors is calculated by giving each type of selector a score. The reason it's laid out this way is because you can combine selectors and the score will increase in each column depending on the number of each type of basic selector used. The end goal is to calculate which rules will be applied to the selected elements.

  ID  |  Class  |  Tag
------|---------|-----
  0   |    0    |   1
  0   |    1    |   0
  1   |    0    |   0

The general rule of thumb, which we'll see over and over again throughout the course, is to keep the specificity of any selector as low as possible.


