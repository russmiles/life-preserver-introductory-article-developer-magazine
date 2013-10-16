# Life Preservation for Adaptable Software

While recently working with one of my clients I realised that there was several questions that I was continually having to answer. These questions were gaining the necessary repetition and weight to start to make me consider them as 'general' problems, and so I decided to see if I could come up with an approach or, even better, a tool to help me overcome them.

In this article I'd like to share the tool and approach I came up with.

## The Questions

First let's look at the questions that kept commonly coming up with my client:

* **Where does my component go?**
* **How do I make sure my components are as simple as possible**
* **How do I visualise and manage coupling in order that it's easier to change my software according to tomorrow's needs, without over-designing!?**

## Where does my component go?

I think it's fair to say that I like circles. This might sound like an odd confession to begin with, but in a moment you'll begin to see what I mean.

To begin my investigation into how to answer the perfectly valid question of "Where does my component go?" I looked first to the typical styles of diagramming used by architects and designers alike.

## The Layered Architecture

The typical layered architecture most common form of diagram used for visualising and conceptualising a piece of software, especially Enterprise software (which I loosely define as software that is built in a company for the exclusive use of that company).

![Typical Layered Architecture Diagram](images/layered-architecture-1.png)

The layered architecture promotes a feeling of 'vertical gravity' in that it feels that each layer is built on top of another. This is fine as far as it goes until the Domain Objects (my definition here is the components that are unique to your application's domain and that do not compromise the expressiveness of your ubiquitous language according to Domain Driven Design) are introduced as a vertical 'elevator-style' 'layer' that bridges the horizontal layers.

![Layered Architecture Diagram with Domain Objects Added](images/layered-architecture-2.png)

## The Problems of the Layered Architecture

Given the popularity of the layered approach to visualising and rationalising about software, what arguments can we really have against it?

The first hint comes from the inevitable response that I get whenever I encounter the layered architecture diagram for a given piece of software and begin to discuss it with the development team.

At some point the team's voice collectively takes on the tone of Bill Lumbergh from ["Office Space"](http://www.imdb.com/title/tt0151804/):

!["Umm, yeah, that's not how the software actually works; that's just for the architecture/designers/insert some other group here"](images/bill-lumbergh.jpg)

What?! We have a diagram, and remember a diagram has power as it does inform our thinking about the software, that is no longer based in reality when it comes to the actual software? So what good is it then?

Even I've used the Layered Architecture diagram approach to communicate about 'typical' software applications before on the courses I often run. However it's also fair to say that generally the students and I recognise that the diagram will rapidly fall apart when the software enters reality and so not a huge amount of attention is heaped upon the diagram. 

In many respects, as the Layered Architecture moves from the world of abstract, layered conceptualising and into the real world of "Where does my component go?", it rapidly moves into an idealistic, a priori existence on some ethereal plane whose only purpose seems to be to make us feel guilty (that the software doesn't 'really' follow that ideal breakdown) and confused (when the layered architecture is attempted to be used to comprehend our software at all).

The Layered Architecture moves into this ghostly realm where it no longer really represents the software any more for two main reasons: It doesn't answer where your component should go, therefore it doesn't end up representing how your components and design of the real software is actually divided up. The Layered Architectural view is a terrible tool for understanding, rationalising and conceptualising your software.

In short, the Layered Architectural view doesn't help you organise your software's component parts to best effect. If anything, it confuses you.

## Surfacing and Decision Making: Introducing Miles' Law*

Architectural and Design Diagrams should aim to support emerging solutions as well as keeping pace with the change to our software. Our diagrams should provides a means of *surfacing* the concerns that need consideration in our design in order to support better *decision making* as the design evolves. These two activities are crucial to producing coherent, clear and comprehendible software that can adapt to the necessary change that it is subjected to during the development process. 

The diagrams we use to visualise and rationalise about our software, alongside a number of other factors, inherently inform the structure of the software we write. 

Miles' Law states that:

> "Diagrams, alongside our understanding of the domain and even the languages and frameworks upon which we rely, are tools for not just expressing how we think about our software but also guiding our thinking in how we approach its architecture and design."

So diagrams are not passive participants in the architecture and design process, they can be enhancing or inhibiting players in the thinking that becomes our software's design. For this reason I believe the Layered Architectural approach is dangerous as it not only confuses when it does not reflect the true breakdown of your software, it also fallaciously and subliminally guides our thinking. We need a better way, especially if we wish our software itself to embrace change…

> * Ok, 'Law' might be going a bit far here, but if [Conway's Law](http://en.wikipedia.org/wiki/Conway's_law) states that "organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations", then I'm fairly confident that my own law, that our means of visualising and rationalising about our software has a direct impact on the design of our software, will stand the test of time also.

## Why Adaptability Matters

*Change* is an inevitable force upon your application's structure and, more importantly, on the assumptions you have made to-date that comprise the structure of your software.

Change is a ubiquitous and accelerating force that is often comes from a number of sources including:

* Discovery of the need for new functionality; we'll call this *Extension* of your application.

* A clearer understanding is achieved of the existing, possibly erroneous, functionality; we'll call this *Amendment* of your software.

Either of these two types of change potentially has the power to   cause significant pain when architecture, design and implementation is approached.

A common anecdote that effectively explains what we mean by change would be:

> You experience the true pain of change when someone simply asks "Can you make this small change here…" and you come close to weeping as the answer that is forced out of you is "It's not that simple…" 

On the other side of the equation, *Adaption* is the reaction that is necessary from the thing, in our case your software, that is the subject of the change. There is a causal relationship between change and adaption; where change is the *cause* and adaption is the *effect*.

When your collective assumptions about future change are aligned with the incoming changes, and your code and it's intention are humanly comprehendible, the impact of necessary adaption can be small. When your assumptions are not aligned with future change, the impact of adaption is large and painful and also the range of adaption options can be reduced.

For the reasons previously mentioned, the Layered Architectural approach unfortunately, at a minimum, does not support decisions that help you increase the adaptability of your software design, but can in fact work against it.

## A Better Approach: Thinking of an Island, and a Circle 

While I don't necessarily see the layered architecture dying anytime soon, I think we need a better approach that actually helps us organise our components and ends up being a true and comprehendible reflection of the actual structure of our software.

As a starting point, consider your software conceptually as an island, so following the stereotypically desert island we'll make our software a couple of circles:

TBD Picture of a circle from the tool.

Your software application has a core that represents the components that capture your application's unique domain; in the layered architecture these would be your domain objects. Your domain objects may be organised into many cohesive areas of concern.

To bring this to life we're going to use a concrete example of an Ordering system for a local Noodle Bar, the Yummy Noodle Bar in fact.

![Yummy Noodle Bar](images/yummynoodle.jpg)


## Core and Integration: Life Preservation

TBD Introduce the key characteristics of the core and integration domains. integration being essentially 'compromise' between the evolutionary pace of external systems and application integration, and the core being importantly able to evolve at the pace set by the development teams working directly on this application.

## Organising Concerns and Code with Domains

TBD: Organising and reducing components with a direct mapping to packages.

TBD Packages for Java.

## Simple, Event-Driven Components

TBD Introduce the key characteristics of the components. How they can be reduced down to micro and macro concerns and organised within the package structure.

Lead on to what is the contract between domains? What is the implementation of the boundaries between domains?


## Adaptability through Events and the Event Domain

TBD Talk about events being the documents of exchange between domains, with any number of transformations happening in order to de-couple the domains. Talk about the different types of decoupling. Talk about taking it to tyne limit with data-driven, data structure events and the components implementing Postel's law in order.

## Intent and Events within the Event Domain: CQRS

TBD Talk about the support for CQRS within the event domain.

## A Graceful Increase in Essential Complexity

TBD Now that the event domain is used to declare the exchanges and routing between different autonomous domains, talk here about how the different components in the event domain can be made more complex, introducing patterns such as Disruptor etc.

## (Re) Discovering Hexagonal Architectures

TBD: It just so happens that all this work was not occurring in isolation, and had been nicely preceded by Alistair Cockburn's Hexagonal Architectures.

Arguably breaking the hegemony of the Layered Architecture has simply led to re-discovering the Hexagonal Architectural approach, and the Life Preserver has taken this two steps further by taking advantage of the latest patterns in de-coupling domains using events and Domain Driven Design, while at the same time offering a practical tool for Organising, Reducing and surfacing those concerns and their boundaries/coupling.

## Surfacing and Decision Making

TBD Ultimately the Life Preserver is a surfacing and decision making tool. Run through the steps involved in creating and maintaining one.

## Summary

TBD Recap about the Surfacing and Decision Making capabilities that the Life Preserver brings.

The Life Preserver is just one tool for simplifying your software towards the goal of building software that can embrace change through adaption. This article has been serialised from the ["Simplicity in Software: Principles, Patterns, Practices and Tools for Building Adaptable Software"](https://leanpub.com/simplicityinsoftware) book by [Russ Miles](http://www.simplicityitself.com/consultancy) and [David Dawson](http://www.simplicityitself.com/consultancy) available at [https://leanpub.com/simplicityinsoftware](https://leanpub.com/simplicityinsoftware). An accompanying course or working is also available if you register an interest at [http://www.simplicityitself.com/courses](http://www.simplicityitself.com/courses).

Interesting in seeing how the Life Preserver can be implemented in real code? Check out the current and forthcoming samples that are being published to the [Simplicity Itself tutorials section](http://www.simplicityitself.com/tutorials). 

Many of these examples show how to effectively implement each of the domains and sub-domains that your own Life Preserver will capture using the [Spring Portfolio](http://www.spring.io), however it's important to remember that the Life Preserver approach and tool, along with the ideas of simple event-driven components, are entirely agnostic to your choices of implementation technology.

## Author Biography



