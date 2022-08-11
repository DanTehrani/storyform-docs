# Create a form

#### You can create a form here, by providing a JSON representation of your form. The JSON should follow the specification described below.





### The JSON should adhere to the following structure

#### Example

```json
{
  title: "Title of your form",
  questions: [
    {
      label: "First question",
      type: "text",
      customAttributes: []
    },
    {
      label: "Second question",
      type: "select",
      options: ["option 1", "option 2"],
      customAttributes: []
    }
  ]
}
```

#### Form

<table><thead><tr><th>prop</th><th>description</th><th data-type="select">required/optional</th></tr></thead><tbody><tr><td>title</td><td>The title of the form</td><td></td></tr><tr><td>questions</td><td>An array of questions. A question should follow the structure specified below.</td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>



Question

<table><thead><tr><th></th><th></th><th data-type="select">required/optional</th></tr></thead><tbody><tr><td>label</td><td>The label of the question</td><td></td></tr><tr><td>type</td><td><p>One of the followings:</p><p>type, select</p></td><td></td></tr><tr><td>options</td><td>An array of options.</td><td></td></tr><tr><td>customAttributes</td><td>An array of strings, that are meant to be used by custom interfaces.</td><td></td></tr></tbody></table>





