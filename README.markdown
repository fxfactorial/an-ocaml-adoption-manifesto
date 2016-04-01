OCaml 2016 -- The State of the Hump
========================================

It's 2016 and we all know functional programming is the path forward.
From ReactJS, Elixir, MirageOS, Docker, and Facebook flow to Elm, this
style of programming is clearly being widely adopted and needed.

This is my biased viewpoint coming from working in a startup in San
Francisco and from running the OCaml meetup group in Silicon
Valley. It's an expression of my frustations in the current
environment from speaking to absolute programming beginners to
experienced JavaScript programmers (and every variant of C in
between). It is not a criticism of any one person or organization,
but a critique from a love of the community and OCaml itself.

Getting to the Next Stage
=============================

Tools like `opam` and `merlin` were desparately needed and got us past
what I'd call the first hump, but now we need to get past the second
hump; to capture that group of programmers that just need to have a
`json` based HTTP request to work (1 line of code in Python, at least
10 in OCaml + talk about monads). I'm talking about folks that look to
introductions to functional programming in Python/JavaScript instead
of going directly to OCaml.

What's missing for wide spread adoption
=============================================

Here's the TODO list, order doesn't mean priority.

These issues also overlap with why a typical SV startup might hesitate
to pick OCaml (Some of these issues are being worked on).

1. An actual ORM. Wrong or right they get stuff done. A nice feature
   would be something that used a PPX extension to generate type safe
   SQL and functorized over a backend, starting with
   `Postgresql`. Just hasn't been done. There are things that
   approximate this but they have various short comings in their own
   way. Maybe something like `[@@deriving pg_insert, pg_select]`
   (thanks `hcarty`).

2. Typical middleware needed for web application backends. We need
   something like `nodejs`'s express. Something that instantly handles
   30k+ connections, like I can with 30 lines of `JavaScript` in Node.

3. Documentation, documentation, documentation. We have amazing tools
   like `js_of_ocaml` but the documentation is lacking and only the
   most determined hackers stay.

4. A web framework in the spirit of Django or Rails. (And please not
   something that reaches `Yesod` levels of mental
   abstraction).

5. `js_of_ocaml` or `bucklescript` bindings to `ReactJS`, that would
   be ideal.

6. Namespaces. This is a problem right now, name something `dispatch.ml`
   and use a transitive dependency that also defines dispatch. Boom.

7. A friendlier attitude towards web development. Many people still
   think web coding is lame or not serious. That's wrong, web
   programming is amazing and much innovation comes out of web
   programming.

8. Core libs like `Lwt` need love and care, and there are simply not
   enough hands to go around at the moment and that's a real shame
   since big projects like `mirage` are built on top of `Lwt`.

9. Marketing. Haskell blows us out of the water in name recognition,
   and there's no reason why we can't have that level of recogition
   as well.

10. The build situation is pretty bad. We have too many build tools
    with no consensus on building code. Explaining all of them at once
    to programmers coming from interpreted languages is a big time
    suck.

11. Windows support.

12. A non-monadic HTTP library, maybe `cohttp.unix`.

13. Multicore.


Issues Noted by Others (Send a PR to add one!)
====================================================

1. A way to develop *native* mobile applications in OCaml, allowing to
    use standard and huge native libraries in Swift, Java or
    C#. Mobile applications became a real need for companies and it
    costs to have to hire several developers for each platform. A
    compiler source to source with an intermediate language between
    Swift, Java and C# could be a solution.

2. IDE support. Decent Intellij Idea or Eclipse plugin would
   accelarate the adoption.

Optimism
=========

The more people we can get into OCaml, the more these problems go
away -> more people means more $$$ and hands.

The OCaml community is made up of many friendly and incredibly
talented people. I'm sure we can overcome these difficulties. 2016 is
going to be OCaml's year, no doubt.
