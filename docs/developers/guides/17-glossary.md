---
title: Glossary
layout: doc_page.html
order: 17
---

## Recipe

- Executable
- Functional tests (with framework, node, docker)
- General Configuration: (piscosour.json) Implementation of all steps, dependencies to flows.
- No steps, no plugins, no contexts, no flows allowed.
- Dockerizable
- Implementation of same step of same context is forbidden.
- Multi-domain. Can execute a command , if command es the same in more than one domain then shows a list to choose the right one.
- Two plugins with the same name in a recipe should give an error.
- Array domains with all allowed domains to be listed in commands. (default: all)
- Dependency to all flows implemented. Repeated flow name in same recipe is not allowed.   

## Plugins

- NO tag domain
- Only implementation of one or more plugins
- Unit tests with framework
- Dependency to piscosour on devDependency
- No general configuration (piscosour.json). No estoy muy seguro de esto.

## Steps (commands)

- Tag domain
- Only implementation of one or more steps
- Unit tests with framework
- Dependency to piscosour on devDependency
- Dependency to definition of contexts on devDependency

## Contexts

- Tag domain
- Only implementation of one or more contexts
- Unit tests with framework
- Only definition of contexts
- Could have other contexts as a dependency and is possible to extend individual contexts.

## Flows

- No tag domain. Flows is not inside a domain are dependencies of a recipe.
- Only definition of flows

## Domain

- Domain is a tag on every steps and contexts repositories.

In same domain:

- Repeated step name is forbidden
- Repeated context name is forbidden
 
## Configuration

- Only General configuration (piscosour.json) 
- And dockerfiles directory for Dockerfile implementation for requirements.