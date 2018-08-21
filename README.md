> Cypress + Docker + GitLabCI = ❤️

[![pipeline status](https://gitlab.com/cypress-io/cypress-example-docker-gitlab/badges/master/pipeline.svg)](https://gitlab.com/cypress-io/cypress-example-docker-gitlab/commits/master)

Running your Cypress E2E tests on GitLab CI is very simple. You can either
start with a base image or with an image that already includes Cypress tool.

## Base image

You can derive your custom CI image from
[cypress/base](https://hub.docker.com/r/cypress/base/) and install
`cypress`. Here is a typical `.gitlab-ci.yml` file

```yaml
image: cypress/base:10
cypress-e2e:
  script:
    - npm install
    - $(npm bin)/cypress run
```

See [.gitlab-ci.yml](.gitlab-ci.yml) for more realistic setup with caching and parallel jobs

See [Cypress Continuous Integration](http://on.cypress.io/continuous-integration) documentation for more information.

## Happy testing

If you find problems with Cypress and CI, please

- consult the [documentation](https://on.cypress.io)
- ask in our [Gitter channel](https://gitter.im/cypress-io/cypress)
- find an existing [issue](https://github.com/cypress-io/cypress/issues)
  or open a new one
