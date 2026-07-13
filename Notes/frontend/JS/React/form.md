

# React Forms

## What are Forms?

Forms are used to collect input from users.

Examples: - Login Form - Registration Form - Contact Form - Feedback
Form

In React, form data is usually controlled using **state**.



## Controlled Component

A controlled component means React controls the value of the input.

### Syntax

``` jsx
const [name, setName] = useState("");

<input
  type="text"
  value={name}
  onChange={(e) => setName(e.target.value)}
/>
```



# React Forms Submit

When a form is submitted, React usually prevents the page from
refreshing.

### Syntax

``` jsx
function App() {
  const [name, setName] = useState("");

  function handleSubmit(event) {
    event.preventDefault();
    alert(name);
  }

  return (
    <form onSubmit={handleSubmit}>
      <input
        value={name}
        onChange={(e)=>setName(e.target.value)}
      />

      <button type="submit">
        Submit
      </button>
    </form>
  );
}
```

### Why use preventDefault()?

Normally, forms refresh the page.

`event.preventDefault()` stops that behavior.


# React Textarea

Instead of writing text inside `<textarea>`, React uses the value
attribute.

### Syntax

``` jsx
const [message, setMessage] = useState("");

<textarea
  value={message}
  onChange={(e)=>setMessage(e.target.value)}
/>
```



# React Select

The selected option is also controlled by state.

### Example

``` jsx
const [city, setCity] = useState("Bangalore");

<select
  value={city}
  onChange={(e)=>setCity(e.target.value)}
>
  <option>Bangalore</option>
  <option>Mysore</option>
  <option>Mumbai</option>
</select>
```



# React Multiple Inputs

Large forms usually contain multiple fields.

Instead of creating multiple states, we can store everything inside one
object.

### Example

``` jsx
const [formData, setFormData] = useState({
  name: "",
  age: ""
});

function handleChange(event){
  const {name, value} = event.target;

  setFormData({
    ...formData,
    [name]: value
  });
}
```

Inputs

``` jsx
<input
 name="name"
 value={formData.name}
 onChange={handleChange}
/>

<input
 name="age"
 value={formData.age}
 onChange={handleChange}
/>
```


# React Checkbox

Checkboxes store true or false values.

### Example

``` jsx
const [checked, setChecked] = useState(false);

<input
 type="checkbox"
 checked={checked}
 onChange={(e)=>setChecked(e.target.checked)}
/>
```

Output

    true
    false



# React Radio Buttons

Radio buttons allow selecting only one option.

### Example

``` jsx
const [gender, setGender] = useState("");

<input
 type="radio"
 value="Male"
 checked={gender==="Male"}
 onChange={(e)=>setGender(e.target.value)}
/>

<input
 type="radio"
 value="Female"
 checked={gender==="Female"}
 onChange={(e)=>setGender(e.target.value)}
/>
```


# Common Form Events

  Event      Purpose
  ---------- ----------------------
  onChange   Detect input changes
  onSubmit   Form submission
  onFocus    Input selected
  onBlur     Input loses focus
  onClick    Button clicked



# Best Practices

-   Always use controlled components.
-   Store form values in state.
-   Use preventDefault() while submitting.
-   Use one object for large forms.
-   Validate user input before sending data.
-   Give meaningful input names.



# Quick Revision

-   Forms collect user input.
-   useState stores form values.
-   onChange updates the state.
-   onSubmit handles form submission.
-   preventDefault() stops page refresh.
-   Textarea uses value.
-   Select uses value.
-   Checkbox stores true/false.
-   Radio buttons select one option.
-   Large forms are easier using one state object.

