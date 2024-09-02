There are three different types of Models when it comes to UML (Universal Modeling Language):

1. Computational models, which can be computer simulations representing time-varying behaviour of a system
2. Analytical models, which are mathematical models of relationships among variables in a system
3. Nonanalytical/descriptive models, which are models that describe componenets and their relationships to them

Class Diagrams are used to mdel the types of objects and relationships among them, and are one of the most commonly used diagrams that can, and are, drawn by developers as part of design activity

The key elements in class diagrams can be divided into three groups: 

1. Classifiers, represent the types of entities in the system
2. Features, represent the structural and behavioural characteristisics of these entities
3. Relationships, depict how these entities are related to one another

===================================
Classifiers
===================================


The technical definition of a Classifier is an abstract metaclass whose concrete subclasses classify different types of values, such as:
- Concrete class      - Enumerations
- Abstract class      - Generic class
- Interface

All classifiers are denoted as a box with three compartments, with a name in the top compartment, whilsthe bottom two compartments are for listing the features of the classifier itself.

===================================
Features
===================================

Features provide the structural behaviours and characteristisics of classifiers. Features can be Structural, meaning that only the properties & attributes are EXCLUDED from the middle component of the classifier notation, or they can be Behavioural, meaning that it is the operations themselves, or methods, that go into the bottom component of the classifier box.

===================================
Relationships
===================================

Relationships bring all the classifiers together to make the system work, for example, Relationships show the interdependency of classes, with those same classes inhereting from each other or implementing interfaces or abstract classes, with these Relationships being grouped into three categories:

1. Associations
2. Generalizations
3. Dependencies

===================================
Deriving class diagrams
===================================

 Imagine you have a scheduling system in which an Event-organizer in some organization wants to organize an event, and for that, she wants to book at venue. The system is supposed to offer the functionality of booking a venue for an event, which makes a use case as Book event-venue. In its basic scenario, the Event-organizer submits a request to book a venue. The request reaches a Venue-caretaker and a Parking-manager. The Venue-caretaker looks at various details of the request and approves if everything seem okay. Similarly, the Parking-manager also approves a request. After which, the Event-organizer confirms a venue booking. So:

 1. **Event-organizer** <ins>creates</ins> a **request** for a **venue** and <ins>submits</ins> it with **event** details:
        _Event name_, _event type_, _date_, _time_, _duration_, _audience-size_, _venue-name_

2. **Venue-caretaker** and **Parking-manager** receive</ins> the request.
3. Venue-caretaker <ins>approves</ins> the request for the venue
4. Parking-manager <ins>approves</ins> the request for **parking** for the given audience-size
5. Event-organizer <ins>confirms</ins> the event-venue

===================================

So:

My **Classifiers** are:

**Event-organizer**
**Request**
**Venue**
**Event**
**Venue-caretaker**
**Parking-manager**
**Parking**

My _Attributes_ are:

Request: _Event_
    Event: _Event-name_,
    Event: _Event-type_,
    Event: _Date_,
    Event: _Time_,
    Event: _Duration_,
    Event: _Audience-size_,
    Event: _Created-by_,

Venue: _Venue-name_

My <ins>Relationships</ins> are:
- **Event-organizer** <ins>creates</ins> **Request**
- **Event-organizer** <ins>submits</ins> **Request**
- **Venue-caretaker** <ins>receives</ins> **Request**
- **Parking-manager** <ins>receives</ins> **Request**
- **Venue-caretaker** <ins>approves</ins> **Request**
- **Parking-manager** <ins>approves</ins> **Request**
- **Event-organizer** <ins>confirms</ins> **event-venue**

In regards to actually creating these diagrams, explicitly referencing the specifiation(s) given above, however, one important thing to note is that when given a specifications, I can look for all the _nouns_, as they represent potential candidates for my classifiers, or the entities that will become apart of my system. So, given the text above, I would have seven of these classifiers, keeping in mind that I'm using nouns such as the users' roles within the business structure: Event-organizer, the things they work on (_like a request or venue_).

Next, I want to identify the attributes _of_ these classifiers, and, referencing the text again, I can identify atrributes for just three of my classifiers: **request**, **event**, and **venue**. If I were to continue this analysis of the text for use cases, such as posting/registering for an event, then more attributes would emerge.

Finally, I want to identify the verbs which are indicative of some kind of relationships amongst these classifiers. These relationships would then model the behavioural features of my classifiers.
