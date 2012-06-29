# jquery-columnlist

jQuery plugin for splitting up uls into equal lists

## Options
* `size`: How many columns to split the UL into. If left blank, will check the UL's `data-column-list` attribute.
* `class`: Class appended to the new sub ULs
* `incrementedClass`: Class appended to the new sub ULs with an incremented suffix, i.e. 'column-list-2'

## Example

```javascript
    $('ul.column-list-js').columnlist({
        size : 3,
        'class' : 'column-list',
        incrementClass : 'column-list-'
    });
```

Turns this...

```html
    <ul class="column-list-js">
        <li>Item #1</li>
        <li>Item #2</li>
        <li>Item #3</li>
        <li>Item #4</li>
        <li>Item #5</li>
        <li>Item #6</li>
        <li>Item #7</li>
        <li>Item #8</li>
    </ul>
```

Into this...

```html
    <ul class="column-list-js">
        <li class="column-list-0 column-list">
            <ul>
                <li>Item #1</li>
                <li>Item #2</li>
                <li>Item #3</li>
            </ul>
        </li>
        <li class="column-list-1 column-list">
            <ul>
                <li>Item #4</li>
                <li>Item #5</li>
                <li>Item #6</li>
            </ul>
        </li>
        <li class="column-list-2 column-list">
            <ul>
                <li>Item #7</li>
                <li>Item #8</li>
            </ul>
        </li>
    </ul>
```

## Contributing

This project uses [smoosh](https://github.com/fat/smoosh) for compiling, linting.
