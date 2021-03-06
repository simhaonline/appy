---
description: Covers what each folder is being used for.
---

# Folder Structure

```bash
.
├── .docker                        (the docker related files)
│   ├── Dockerfile                 (for building the docker image)
│   ├── Dockerfile.dockerignore    (for excluding the files/folders when building the docker image)
│   └── docker-compose.yml         (for running the databases in docker containers locally)
├── .editorconfig                  (for maintaining consistent coding styles for multiple developers working on the same project across various editors and IDEs)
├── .gitignore                     (for excluding the files/folders from being version controlled with Git)
├── Makefile                       (for storing frequently used commands that are difficult to memorise)
├── README.md                      (for documenting the project)
├── assets                         (for storing the fonts/images/medias/scripts/styles for both client-side and server-side rendering)
│   ├── fonts
│   │   └── ...
│   ├── images
│   │   └── ...
│   ├── medias
│   │   └── ...
│   ├── scripts
│   │   └── ...
│   └── styles
│       └── ...
├── cmd                            (for keeping the custom commands)
│   └── cmd.go
├── configs                        (for keeping the configs of all environments)
│   ├── .env.development
│   ├── .env.test
│   ├── development.key
│   └── test.key
├── db
│   ├── migrate
│   │   └── primary                (for keeping the database migrations for "primary" database)
│   │       └── schema.go
│   └── seed
│       └── primary                (for keeping the database seeds for "primary" database)
│           └── seed.go
├── go.mod                         (the project dependencies for backend)
├── go.sum                         (the project dependencies lockdown versions for backend)
├── main.go                        (the application entry point)
├── nightwatch.conf.js             (the NightwatchJS config for e2e testing)
├── package-lock.json              (the project dependencies for web)
├── package.json                   (the project dependencies lockdown versions for web)
├── pkg                            (the backend logic)
│   ├── app                        
│   │   ├── app.go                 (the application initialization logic)
│   │   ├── asset.go               (the application embedded asset)
│   │   └── config.go              (the application config)
│   ├── graphql
│   │   ├── config.yml             (the gqlgen config, please refer to https://gqlgen.com/config/)
│   │   ├── generated
│   │   │   └── generated.go       (the gqlgen auto-generated boilerplate)
│   │   ├── graphql.go
│   │   ├── model
│   │   │   └── models_gen.go      (the gqlgen auto-generated models)
│   │   ├── resolver
│   │   │   └── resolver.go        (the GraphQL logic for resolving queries/mutations/subscriptions)
│   │   └── schema                 (the GraphQL schemas ended with .graphql/.gql)
│   │       └── ...
│   ├── handler
│   │   ├── handler.go             (the application HTTP handler entry, used to setup global middleware and routes)
│   │   ├── ...                    (the application HTTP handler)
│   │   └── middleware             (the middleware for HTTP handler)
│   │       └── ...
│   ├── job
│   │   ├── job.go                 (the application background job entry, used to setup global middleware)
│   │   ├── ...                    (the application background job)
│   │   └── middleware             (the middleware for background job)
│   │       └── ...
│   ├── locales                    (the backend locales in YAML format)      
│   │   └── ...
│   ├── mailer                     
│   │   ├── mailer.go              (the application mailer entry, used to setup base preview/email)
│   │   └── ...
│   ├── model                      (the application ORM that communicates with the database)
│   │   └── ...
│   ├── viewhelper                 (the server-side view helper)
│   │   └── viewhelper.go
│   └── views                      (the server-side view folder)
│       ├── layouts
│       │   ├── application.html   (the server-side view default layout)
│       │   ├── mailer.html        (the application mailer default HTML layout)
│       │   └── mailer.txt         (the application mailer default TXT layout)
│       ├── mailers                
│       │   ├── welcome.html       (the application mailer HTML template for a specific mailer)
│       │   └── welcome.txt        (the application mailer TXT template for a specific mailer)
│       └── welcome
│           └── index.html         (the application HTML template for a specific handler)
├── svelte.config.js               (the config file for svelte-preprocess)
├── tsconfig.json                  (the config file for Typescript)
├── web                            
│   ├── e2e                        (the NightwatchJS e2e tests, refer to https://nightwatchjs.org/guide)
│   │   ├── custom-assertions
│   │   │   └── ...
│   │   ├── custom-commands
│   │   │   └── ...
│   │   ├── page-objects
│   │   │   └── ...
│   │   └── specs
│   │       └── ...
│   ├── public                     (the public folder which its files will be served at the root)
│   │   └── ...
│   ├── src
│   │   ├── components             (the web components written in SvelteJS)
│   │   │   └── ...
│   │   ├── initI18n.ts            (the web I18n entry)
│   │   ├── initServiceWorker.ts   (the web service-worker entry)
│   │   ├── locales                (the web I18n locales in JSON format)
│   │   │   └── ...
│   │   ├── main.ts                (the web entry)
│   │   ├── pages                  (the web pages written in SvelteJS)
│   │   │   └── ...
│   │   ├── stores                 (the web SvelteJS stores)
│   │   │   └── ...
│   │   └── types                  (the web type definition)
│   │       └── ...
│   └── tests                      
│       └── setup.js               (the web test setup for Jest)
└── webpack.config.js              (the web's webpack config)
```

