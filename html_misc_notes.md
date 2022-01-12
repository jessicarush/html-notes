# HTML miscellaneous notes

## input attributes

```html
<input
  id="ap_password"
  autocomplete="new-password"
  class="simple-form__field simple-form__field--password"
  maxlength="32"
  minlength="8"
  name="ap_password"
  oninvalid="this.setCustomValidity('Passwords should be at least 8 characters long and may not contain quotation marks.')"
  onchange="try{setCustomValidity('')}catch(e){}"
  oninput="setCustomValidity(' ')"
  pattern="[^\x22&quot;&rdquo;&ldquo;]+"
  required="required"
  type="password"
  value=""
>
```

other patterns:

```text
Alphanumeric and may contain underscores and dashes
pattern="[a-zA-Z0-9_-]+"
```