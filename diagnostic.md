# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
  Our example in class is the listr-list and listr-list/items, which come from different pieces of data and render independently. GA, however, might have a
  'cohort' component, and within that have 'students.'
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
  ember g component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
  The component has both a `component` and a `template` file which make up the
  component. The `template` is a handlebars file which determines how the information
  will be rendered on the page, while the `component` takes any manipulation or functions within the component. Together, they are also responsible for data binding.

    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
{{my-contact}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.phone as |phone|}}
        {{my-contact/my-phone phone=phone }}
      {{/each}}
    ```
