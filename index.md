---
layout: default
---


# Importance Driven Coverage of Deep Learning Systems
Deep Learning (DL) systems are key enablers for engineering intelligent applications due to their ability to solve complex tasks such as image recognition and machine translation. 
Nevertheless, using DL systems in safety- and security-critical applications requires to provide testing evidence for their dependable operation. 
Recent research in this direction focuses on adapting testing criteria from traditional software engineering as a means of increasing confidence for their correct behaviour. 
However, they are inadequate in capturing the intrinsic properties exhibited by these systems. We bridge this gap by introducing DeepImportance, a systematic testing methodology accompanied by an _Importance-Driven_ (IDC) test adequacy criterion for DL systems. 
Applying IDC enables to establish a _layer-wise functional understanding_ of the importance of DL system components  and use this information to guide the generation of _semantically-diverse_ test sets. 
Our empirical evaluation on several DL systems, across multiple DL datasets and with state-of-the-art adversarial generation techniques demonstrates the usefulness and effectiveness of DeepImportance and its ability to guide the engineering of more robust DL systems.


### Selected Hyperparameters In Evaluation
**CW:**
```
batch\_size=1,
confidence=0,
learning\_rate=5e-3,
binary\_search\_steps=5,
max\_iterations=1000,
abort\_early=True,
initial\_const=1e-2,
clip\_min=0,
clip\_max=1
```

**FGSM:**
```
 eps=0.3,
 ord=np.inf,
 y=None,
 y_target=None,
 clip_min=None,
 clip_max=None,
 clip_grad=False,
 sanity_checks=True,
```

**BIM:**
```
?
```

**JSMA:**
```
 theta=1.,
 gamma=1.,
 clip_min=0.,
 clip_max=1.,
 y_target=None,
 symbolic_impl=True,
```

**Training Parameters:**
```
loss = 'categorical_crossentropy'
optimizer = 'adadelta'  --> learning_rate=1.0, rho=0.95
metrics = ['accuracy']
batch_size = 256,
epochs = 10
```

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
