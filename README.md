# EngCAS
This repository will be a modification of FriCAS/Axiom. This is a rewrite of FriCAS/Axiom by changing the updating the FriCAS/Axiom language. It is intended that the new language be implemented on alternative implementation languages such as C, Unicon, Python or Scheme instead of the current Common Lisp base as used in FriCAS/Axiom.

FriCAS/Axiom and other CAS systems can be used for Engineering purposes. However, there are aspect of Engineering model development and claculations that are not easily amenable within these CAS systems.

One of those aspect relates to making sure that the units being used are actually compatible with each other. Whether this be on both sides an equation or within some polynomial description of the model. 

None of these systems appear to have any sort of comprehensive physical unit functionality available as a basic part of the CAS itself. You have to add this on top of the existing system.

Frink is a system that allows at a basic level the use of physical units and it keeps track of these during all phases of the calculations. Any mismatches are highlighted as you write your code. However, Frink does not incorporate many of the basic functionalities available in the more popular CAS systems.

There is a secondary problem within many of these CAS systems, which can come back and bite the user. The axioms in use for different domains have to be incorporated manually by the user and even though, in many cases, these are documented within the CAS systems, there is no functionality provided to have these axioms specified and used by the CAS system itself. The programmer must be aware at times what and how thses axioms apply.

Metamath allows axioms and theorems to be specified and checked and used. Such an enhancement for CAS system would be further beneficial to the broader community of potential users of these CAS systems.

There has been excellent work dome by various users of these systems to make particular CAS systems available for non-mathematicians. One such example is the series Maxima By Example by Edwin Wollett. BUt not all CAS systems appear to have this kind of material available for Engineering oriented users.

This development is based on the shoulders of many giants in the past and present for and by which none of this present work would even be possible.

## Stage 1

This will initially consist of updating the FriCAS language. This will include a different syntactic structure and a more comprehensive denotational semantics. 

On an inital review of the SPAD and BOOT systems, I believe there are far too many Common Lisp quirks that bleed into the FriCAS system. I have undertaken some analysis and it appears that the current parser (Pratt parser) can be incorporated into a LR parser where we can utilise the best of each. This is especially true for the inclusion of new operators and the changing of precedence for those operators based on the specific domain being used.

## Stage 2

Addition of basic physical unit facilities into the system.

## Stage 3

Alternative implementations using various implementation languages.

