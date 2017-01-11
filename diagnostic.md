# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    You could have a recipe book modeled with components.  A list of all recipes that you can click on, and then
    within each, a list of different ingredients.  Each piece would be it's own component because
    they're repeatable.  One recipe will look the same as another and each will contain a list of
    ingredients which again will all look the same.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    When a component is generated, it creates a template file which is what is displayed to the user and
    a component.js file which contains javascript code related to that template and any actions
    you may want to have (ex. creating, deleting, editing, etc.).
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{#each model as |contact|}}
      {{my-contact contact=contact}}
    {{/each}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.phone as |phone|}}
      {{my-contact/my-phone phone=phone}}
    {{/each}}
    ```
