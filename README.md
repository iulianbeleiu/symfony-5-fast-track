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
