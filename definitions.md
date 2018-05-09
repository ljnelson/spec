# Definitions

## Occurrence

_Occurrence_ is a deliberately non-technical term used to describe a
change of state in a computer or non-computer system.  In this
specification, an occurrence is opaque, that is, not further
specified.

An occurrence occurs at a particular authoritative time.

An example of an English description of an occurrence might be: "The
temperature sensor entered the 'battery low' state at
2018-05-09T15:30:00Z."

Another example of an English description of an occurrence might be:
"The virtual machine named 'fred' indicated at 2018-05-09T15:30:00Z
that it will perform a scheduled reboot in the near future."

An occurrence might be identified, uniquely or otherwise, in the real
world by some mechanism, but that mechanism is not specified in this
document.

## Event

Occurrences are represented by _events_.  More specifically, an
_event_ is a concept specified by this specification that represents
an occurrence in a manner such that computer systems may be
programmatically notified that the occurrence has taken place.

An event has _event attributes_, described below.

An event has _event data_, described below.

Two events are conceptually never equal.

## Event Attributes

_Event attributes_ are data specified by this specification that
describe the event itself, separate from its data.

Event attributes are of exactly two kinds: _event metadata_ and _event
context attributes_.

### Event Metadata

_Event metadata_ are event attributes concerning details about the
event itself, such as aspects related to its transmission and location
in time.

Briefly, and non-normatively, event metadata are data about the event,
not the occurrence it describes.

### Event Context Attributes

_Event context attributes_ are event attributes concerning details
about the representation, formatting and encapsulation of the _event
data_ that the event they are part of contains.  These are
distinguished from _event metadata_ by the fact that they may be
conceptually shared between two events.

Briefly, and non-normatively, event context attributes are data about
the representation of the event data within the event, not about the
event itself, nor about the event data itself, nor about the occurrence
the event describes.

## Event Data

_Event data_ is the mostly opaque data that an event carries within
it, representing, in a fashion partially defined by the event context
attributes, the occurrence that the event describes.
