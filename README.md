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


```
