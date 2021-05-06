# Click to show hidden field

Alpine.js is a minimal framework for manipulation behaviour in the browser. [https://github.com/alpinejs/alpine](https://github.com/alpinejs/alpine).

`x-data` declares a scope for that component. `x-show` toggles display none. `x-on:click` defines the behaviour on click.

```
<div x-data="{ show_edit: false }" >
  <i class="fas fa-plus" x-show="show_edit == false" x-on:click="show_edit = true"></i>
  <div x-show="show_edit == true" x-on:click="show_edit = false">Edit
    <i class="fas fa-check text-green-500" x-on:click="show_edit = false"></i>
    <i class="fas fa-times" x-on:click="show_edit = false"></i>
  </div>
</div>
```