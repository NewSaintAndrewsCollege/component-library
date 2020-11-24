---
component: Notification
---
<p class="uk-text-lead">Create toggleable notifications that fade out automatically.</p>

## Usage

The notification will not fade out but remain visible when you hover the message until you stop hovering. You can also close the notification by clicking it. To show notifications, the component provides a simple JavaScript API. The following code snippet gets you started.

### JavaScript

```js
UIkit.notification({
    message: 'my-message!',
    status: 'primary',
    pos: 'top-right',
    timeout: 5000
});

// Shortcuts
UIkit.notification('My message');
UIkit.notification('My message', status);
UIkit.notification('My message', { /* options */ });
```

{% include example.html content='
<button class="demo uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Notification message16&quot;})">Click me</button>

' %}

***

## HTML message

You can use HTML inside your notification message, like an icon from the Icon component.

```js
UIkit.notification("<span uk-icon='icon: check'></span> Message");
```

{% include example.html content='
<button class="uk-button uk-button-default demo" type="button" onclick="UIkit.notification({message: 16&quot;<span uk-icon=\16&quot;icon: check\16&quot;></span> Message with an icon16&quot;})">With icon</button>

' %}

***

## Position

Add one of the following parameters to adjust the notification's position to different corners.


```js
UIkit.notification("...", {pos: 'top-right'})
```

| Position        | Code                                                |
|:----------------|:----------------------------------------------------|
| `top-left`      | `UIkit.notification("...", {pos: 'top-left'})`      |
| `top-center`    | `UIkit.notification("...", {pos: 'top-center'})`    |
| `top-right`     | `UIkit.notification("...", {pos: 'top-right'})`     |
| `bottom-left`   | `UIkit.notification("...", {pos: 'bottom-left'})`   |
| `bottom-center` | `UIkit.notification("...", {pos: 'bottom-center'})` |
| `bottom-right`  | `UIkit.notification("...", {pos: 'bottom-right'})`  |


{% include example.html content='
<p uk-margin>
    <button class="uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Top Left...16&quot;, pos: 16&quot;top-left16&quot;})">Top Left</button>
    <button class="uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Top Center...16&quot;, pos: 16&quot;top-center16&quot;})">Top Center</button>
    <button class="uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Top Right...16&quot;, pos: 16&quot;top-right16&quot;})">Top Right</button>
    <button class="uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Bottom Left...16&quot;, pos: 16&quot;bottom-left16&quot;})">Bottom Left</button>
    <button class="uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Bottom Center...16&quot;, pos: 16&quot;bottom-center16&quot;})">Bottom Center</button>
    <button class="uk-button uk-button-default" type="button" onclick="UIkit.notification({message: 16&quot;Bottom Right...16&quot;, pos: 16&quot;bottom-right16&quot;})">Bottom Right</button>
</p>
' %}


***

## Style

A notification can be styled by adding a status to the message to indicate a primary, success, warning or a danger status.

```js
UIkit.notification("...", {status: 'primary'})
```

| Style     | Code                                            |
|:----------|:------------------------------------------------|
| `primary` | `UIkit.notification("...", {status:'primary'})` |
| `success` | `UIkit.notification("...", {status:'success'})` |
| `warning` | `UIkit.notification("...", {status:'warning'})` |
| `danger`  | `UIkit.notification("...", {status:'danger'})`  |

{% include example.html content='
<p uk-margin>
    <button class="uk-button uk-button-default demo" type="button" onclick="UIkit.notification({message: 16&quot;Primary message...16&quot;, status: 16&quot;primary16&quot;})">Primary</button>
    <button class="uk-button uk-button-default demo" type="button" onclick="UIkit.notification({message: 16&quot;Success message...16&quot;, status: 16&quot;success16&quot;})">Success</button>
    <button class="uk-button uk-button-default demo" type="button" onclick="UIkit.notification({message: 16&quot;Warning message...16&quot;, status: 16&quot;warning16&quot;})">Warning</button>
    <button class="uk-button uk-button-default demo" type="button" onclick="UIkit.notification({message: 16&quot;Danger message...16&quot;, status: 16&quot;danger16&quot;})">Danger</button>
</p>
' %}

***

## Close all

You can close all open notifications by calling `UIkit.notification.closeAll()`.

{% include example.html content='
<button class="uk-button uk-button-default close" onclick="UIkit.notification.closeAll()">Close All</button>

' %}

***

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](javascript.html#component-configuration)

| Option     | Value   | Default      | Description                                                         |
|:-----------|:--------|:-------------|:--------------------------------------------------------------------|
| `message ` | String  | `false`      | Notification message to show.                                       |
| `status`   | String  | `null`       | Notification status color.                                          |
| `timeout`  | Integer | `5000`       | Visibility duration until a notification disappears.                |
| `group`    | String  | `null`       | Useful, if you want to close all notifications in a specific group. |
| `pos`      | String  | `top-center` | Display corner.                                                     |

***

## JavaScript

Learn more about [JavaScript components](javascript.html#programmatic-use).

### Initialization

This is a `Functional Component` and may omit the element argument.

```js
UIkit.notification(options);
UIkit.notification(message, status);
```

### Events

The following events will be triggered on elements with this component attached:

| Name | Description |
| --- | --- |
| `close` | Fires after the notification has been closed. |

### Methods

The following methods are available for the component:

#### Close

```js
UIkit.notification(element).close(immediate);
```

Closes the notification.

| Name        | Type    | Default | Description                      |
|:------------|:--------|:--------|:---------------------------------|
| `immediate` | Boolean | true    | Transition the notification out. |
