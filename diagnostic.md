# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    nested routes
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    app/application/route.js  => load model to get data
    app/application/template.hbs  => shows what to display on the home page with info on my-app
    app/application/components/my-map/template.hbs  => what to display on the page when you are in the my-app url
    app/application/components/my-app/component.js  => how you want to display the file and any actions you want to add
    app/route.js  => maps your app to a url
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |contact|}}
  {{contacts/my-contact contact=contact}}      
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each model as |phone|}}
    {{my-contact/my-phone number=phone.number}}
    {{/each}}


    ```
