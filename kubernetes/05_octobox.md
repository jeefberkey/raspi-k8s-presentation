<!SLIDE>

# End goal

* [github.com/octobox/octobox](https://github.com/octobox/octobox)
* Ruby on Rails with a PostgresQL backend, and Redis for caching

## Octobox layout

    @@@ render-diagram
    graph LR
      octobox
      postgresql
      redis
      internet

      octobox === postgresql
      octobox === redis
      internet ==> octobox
