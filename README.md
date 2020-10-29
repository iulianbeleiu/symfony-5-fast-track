# Symfony 5 The Fast Track

Create Project

```
symfony new <project-name> --version=5.0
```

Launching a local web server

```
symfony server:start -d
```

Use Maker bundle for Development

```
symfony composer req maker --dev

Discover all generators provided by maker bundle
symfony composer req maker --dev

E.g.
Create controller
symfony console make:controller ConferenceController

Create entity
symfony console make:entity Conference
```

Creating an Entity

```
If you add ? as an answer to the type, you get all supported types
E.g OneToMany

If you want to add more properties just runt the make entity command again
```

Make Migrations

```
symfony console make:migration
```

Update database

```
symfony console doctrine:migrations:migrate
```

Install EasyAdmin

```
1. symfony composer req admin
2. php bin/console make:admin:dashboard (create dashboard)
3. php bin/console make:admin:crud (create crud controllers)

```

Implementing a Subscriber

```
symfony console make:subscriber TwigEventSubscriber
```

Working with forms

```
symfony console make:form CommentFormType Comment

Install Symfony Validator & Doctrine Annotations

symfony composer require symfony/validator doctrine/annotations
```

Scuring Admin Backend

```
symfony composer req security

Create Admin User
symfony console make:user Admin
symfony console make:migration
symfony console doctrine:migrations:migrate -n
Generate password
symfony console security:encode-password
($argon2id$v=19$m=65536,t=4,p=1$f8g6Yv73sYIIRZoRyWhJuA$hNSe5OjLtH9NjiAMJxXzrn9ZztgnyuI3o6+igao8IJ8)

sudo docker exec -it guestbook_database_1 bash
psql -U main
insert into admin values(1, 'admin', '["ROLE_ADMIN"]', '$argon2id$v=19$m=65536,t=4,p=1$f8g6Yv73sYIIRZoRyWhJuA$hNSe5OjLtH9NjiAMJxXzrn9ZztgnyuI3o6+igao8IJ8');

Configuring the Security Authentication
symfony console make:auth
```

Store secrets
```
symfony console secrets:set AKISMET_KEY
```

Testing
```
Create unit test
symfony console make:unit-test SpamCheckerTest

Run tests
symfony run bin/phpunit

For functional tests install
symfony composer require browser-kit --dev

Create functional test
symfony console make:functional-test Controller\\ConferenceController

Install fixtures
symfony composer req orm-fixtures --dev

Load fixtures
symfony console doctrine:fixtures:load
```