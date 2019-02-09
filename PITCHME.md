# BDD Full Stack
---

## e2e tests, executable specs

Disclaimer: Not experts, just interested.

Proof of concept, not best practice.

---

# What is BDD

+++

Behavior Driven Development
* TDD evolution
* Specification by Example
* Common language for all stake holders

Note:
User Stories?  <!-- Who use them, who keeps them up to date, are they in sync with the code? -->
  -> Relate to code? <!-- Do they enforce the code? -->
Merging of Specs and Tests
Stakeholder readable
Living Documentation
The missing link

+++?image=https://www.businessballs.com/theme/remui/pix/businessballs/treeswing/tree-swing-s-hogh.jpg&size=contain

@title[Trying to solve the age old problem]

+++

## At its core

Common language to describe the desired behavior of the system
A way to execute the requirements against the code.

+++

## From the Dan North

>BDD is a second-generation, outside-in, pull-based, multiple-stakeholder, multiple-scale, high-automation, agile methodology. It describes a cycle of interactions with well-defined outputs, resulting in the delivery of working, tested software that matters.

---

# Gherkin and features

Simple and ultra light language for writing executable specifications.

+++?image=https://i.imgur.com/IZioED9.png&size=contain

+++?gist=DesHorsley/9403a3550aa1cfd194ffa0f2906591b1&lang=gherkin&title=Simple Feature

@[1] (Overview and grouping of related scenarios)
@[3-4](Description of the feature, free text, links to tickets and references)
@[6](Scenario/Example: Short description of the business case, provides context to the steps)
@[7-9](Steps, precondition, actions and outcome.)
@[11-14](Multiple scenarios can be used to fully explore the feature)

+++

* Manage feature file length
* Improve reader engagement
* Faster development and maintenance

+++?gist=DesHorsley/a93d97b5586fa27dfca461577becae1c&lang=gherkin&title=Feature with examples

@[2-6](Explain why, not just how)
@[8-9](Business rules and exceptions)
@[18](Use of data tables )
@[19](table headers match fields in scenario)
@[20](Happy day)
@[21](Counter example)
@[22](Exceptions and edge cases)

---?image=https://i.imgur.com/ih2oqJm.png&size=contain

@snap[north]
# @color[white](Cucumber - Why?)
@snapend

@snap[text-white]
@quote[Execute your Gherkin]
@snapend

+++

## Ubiquity 

![Imgur](https://i.imgur.com/d70rp1a.png)

---

# Angular and MuleSoft

* Common front end framework
* Java based back end server

+++

## Features for A Tour of Heroes

[Pickled Tour of Heroes](https://github.com/DesHorsley/angular-tour-of-heroes)

* Maintain a list of your favourite heroes
* Top heroes
* Delete

+++

## Steps

* Throw away canary test - `app.steps.ts`
* Dashboard: `dashboard.steps.ts` - Single page, basic operation
* manageHeroes: `manageHeros.steps.ts` - Multiple pages, search by text, clicks buttons
+++

## Intercept API calls

Use of [angular-in-memory-web-api](https://github.com/angular/in-memory-web-api)
Not feature toggled in the sample code but can be

```javascript
@NgModule({
  imports: [
  environment.production ?
    [] : HttpClientInMemoryWebApiModule.forRoot(InMemHeroService)
```

---

# Features for backend

+++

## What is MuleSoft?

<!--Picture of Max the mule or the mule logo? -->

+++

## Steps

+++

## Responding to API calls

+++

# Related Resources

All of these sites came in useful while putting this presentation together:
* [inviqa](https://inviqa.com/blog/bdd-guide) Bdd guide
* [cucumber](https://cucumber.io) Cucumber home page + reference materials
* [John Papa's Tour of Heroes](https://github.com/johnpapa/angular-tour-of-heroes) basis for Angular demo

---

# Presentation Tools
* [gitpitch](https://gitpitch.com)
* [wordclouds](https://www.wordclouds.com/)
