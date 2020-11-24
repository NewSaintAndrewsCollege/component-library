---
component: Spinner
---
<p class="uk-text-lead">Create an animated loading spinner.</p>

## Usage

To create a spinner, add the `uk-spinner` attribute to a block element.

```html
<div uk-spinner></div>
```

{% include example.html content='
<div uk-spinner></div>
' %}

## Ratio

Add the `ratio: 3` parameter to the `uk-spinner` attribute to triple its size – or any other number, depending on how big you want the spinner to be.

```html
<div uk-spinner="ratio: 3"></div>
```

{% include example.html content='
<span class="uk-margin-small-right" uk-spinner="ratio: 3"></span>
<span uk-spinner="ratio: 4.5"></span>
' %}
