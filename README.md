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

TBD Picture of a layered architecture.

The layered architecture promotes a feeling of 'vertical gravity' in that it feels that each layer is built on top of another. This is fine as far as it goes until the Domain Objects (my definition here is the components that are unique to your application's domain and that do not compromise the expressiveness of your ubiquitous language according to Domain Driven Design) are introduced as a vertical 'elevator-style' 'layer' that bridges the horizontal layers.

TBD Picture of the Layered architecture with Domain Objects vertical 

## Problems of the Layered Architecture

Given the popularity of the layered approach to visualising and rationalising about software, what arguments can we really have against it?

The first hint comes from the inevitable response that I get whenever I encounter the layered architecture diagram for a given piece of software and begin to discuss it with the development team.

At some point the team's voice collectively takes on the tone of Bill Lumbergh from the film, ["Office Space"](http://www.imdb.com/title/tt0151804/):

* "Umm, yeah, that's not how the software actually works; that's just for the architecture/designers/insert some other group here"

What?! We have a diagram, and remember a diagram has power as it does inform our thinking about the software, that is no longer based in reality when it comes to the actual software? So what good is it then?

To be fair, I've used the Layered Architecture diagram approach to communicate about 'typical' software applications before on the courses I often run. However it's also fair to say that generally the students and I recognise that the diagram will rapidly fall apart when the software enters reality and so not a huge amount of attention is heaped upon the diagram. 

In many respects, as the Layered Architecture moves from the world of abstract, layered conceptualising and into the real world of "Where does my component go?", it rapidly moves into an idealistic, a priori existence on some ethereal plane whose only purpose seems to be to make us feel guilty (that the software doesn't 'really' follow that ideal breakdown) and confused (when the layered architecture is attempted to be used to comprehend our software at all).

The Layered Architecture moves into this ghostly realm where it no longer really represents the software any more for two main reasons: It doesn't answer where your component should go, therefore it doesn't end up representing how your components and design of the real software is actually divided up. The Layered Architectural view is a terrible tool for understanding, rationalising and conceptualising your software.

In short, the Layered Architectural view doesn't help you organise your software's component parts to best effect. If anything, it confuses you.

## Introducing Miles' Law*

The diagrams we use to visualise and rationalise about our software, alongside a number of other factors, inherently inform the structure of the software we write. 

Diagrams, alongside our understanding of the domain and even the languages and frameworks upon which we rely, are tools for not just expressing how we think about our software but also how we approach its architecture and design.

> * Ok, 'Law' might be going a bit far here, but if [Conway's Law](http://en.wikipedia.org/wiki/Conway's_law) states that "organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations", then I'm fairly confident that my own law, that our means of visualising and rationalising about our software has a direct impact on the design of our software, will stand the test of time also.


## A Better Approach: Thinking of an Island, and a Circle 

Got here.

## Core and Integration: Life Preservation

## Simple, Event-Driven Components

## Adaptability through Events

## (Re) Discovering Hexagonal Architectures

## Summary

## Author Biography


