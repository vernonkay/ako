# The concept: a camera tutor that is safe at a lathe

This is the idea in more detail than the README: what a session feels like, and the
design choices that let an AI coach a beginner at a dangerous machine without ever
touching it.

## A session, from the learner's side

You set up a camera and a microphone looking at your lathe and your working position. You
load a project, say "face and turn a spacer". ako talks. It walks you through the setup,
watches you do each step, and tells you when something is off: a chuck key still in the
chuck, a sleeve hanging loose, a hand drifting toward the work. When it cannot see
something well enough to judge, it does not bluff, it asks you to measure it and say the
number out loud. You work, it watches and coaches, and across a series of projects you go
from "I have never touched one of these" to "I can make that part".

The teacher is patient, it never has somewhere else to be, and it never looks away. That
is the whole point: the thing a lone beginner lacks is not information, there is plenty of
that online, it is a second set of eyes that notices the dangerous thing in the moment.

## The safety inversion

Most people assume an AI at a machine would be dangerous because it might do the wrong
thing. ako is built the other way round. It cannot do anything to the machine at all, by
design, so the only question is whether it is a useful observer. And a camera turns out to
be good at exactly the safety-relevant things a lone learner gets wrong: is the chuck key
still in, is something loose that could catch, is a hand where it should not be, is the
spindle still turning when the learner thinks it has stopped.

So safety is not a disclaimer bolted on the side. It is the first feature, and the one a
camera is genuinely well suited to.

## The three commitments, as mechanisms

The README states three commitments. Here is how each becomes a concrete design rule.

**Coach, never control.** ako has no electrical connection to the lathe. It issues no
command that stops or starts the machine, and it never declares the machine safe to start
or the spindle safe to approach. It states what it observed and asks the human to act.
Only the human stops a manual lathe, and ako is architected around that rather than
treating it as a limitation to work around.

**The operator stays the thinker.** Perception has a honest ceiling. Rather than pretend
past it, ako hands those tasks back: "present the micrometer to the camera and read it to
me", "work out the spindle speed for this diameter and tell me what you chose". The
learner does the reasoning. This is better engineering (no silent false readings) and
better teaching (people learn a craft by doing the thinking, not by being told the
answer).

**Fail safe.** On any uncertain or occluded reading, ako withholds approval and asks the
human. A false "that part is secure" or a missed hand is the expensive failure, so every
ambiguous judgement resolves toward "not yet, check again", never toward reassurance.

## Certification before cutting

Before ako unlocks any cutting, the learner passes a camera-verifiable machine-control
certification. The idea is borrowed from how makerspaces run a lathe checkout, a human
watches you prove you can work the machine safely, and ako can be that observer,
continuously, in a way a busy human instructor cannot.

The gate certifies a reflex, not a quiz. The documented way people are hurt is reaching
for the wrong control under stress, so the keystone is a stop-on-command drill: at a
random moment ako says "stop now", and the learner has to hit the right stop cleanly,
several times in a row. Around that sit checks you can actually verify with a camera and a
microphone: naming the machine's stops, proving you can reach the fastest one from your
working stance, bare hands and secured clothing, the chuck key out of the chuck before any
start, and keeping hands clear while the spindle runs. Each check is rated honestly for
whether a camera can confirm it today; the ones that are marginal run in a narrated mode
(you say what you did, ako confirms) until the perception is proven. The certification is
continuous, not a one-off: the wearable and habit checks re-assert during real work, and
the whole gate re-runs on a trigger, a near-miss, a glove appearing, a long layoff.

## What the camera can and cannot do

ako leans only on perception that is robust today, and is explicit about the rest. Roughly:

- **Reliable now:** a hand or glove present, the chuck key in the chuck, the spindle
  turning or stopped, reading a digital readout at close range with markers, and, from the
  microphone, telling a clean cut from chatter and recovering the spindle speed from the
  sound.
- **Marginal:** gross setup checks, a measurement read at a distance, rough centre height.
  These lean on narration and markers.
- **Not yet, and maybe a teaching moment for a long time:** cut depth, diameter off
  spinning work, surface finish, fine spatial judgements. These are where the operator
  stays the thinker.

Audio deserves a mention because it is cheap and underused: the sound of a lathe carries a
lot (a clean cut versus chatter, the spindle speed) and needs none of the spatial
reasoning that vision struggles with.

## The skill ladder

Guided projects hang off a stable progression, each level unlocking the next:

0. Machine control and safety (the certification above).
1. Facing and turning to a shoulder.
2. Parting and drilling.
3. Tapers and knurling.
4. Boring and reaming.
5. Single-point threading.
6. Precision multi-operation parts.

A guided project is the unit of learning: ordered steps, the skills it teaches, the
hazards to watch, the mastery checks, and the explicit points where ako hands the thinking
back to the operator.

## Why this is a new project, not a fork

An open-source scan found no project that combines the three things ako needs: the
manual-machining domain, a coach that verifies but never actuates, and a graded realtime
see-and-coach loop. The nearest neighbours are realtime voice-and-vision frameworks
(built to be depended on, not forked), fitness and sports form-coaches (the right pattern,
the wrong domain), screen-based tutors (pedagogy but no perception), and camera-based
workshop-safety systems, every one of which stops or controls the machine, which is
exactly the line ako refuses to cross. So ako builds on the frameworks and owns the parts
that do not exist anywhere: the safety contract, the curriculum, and workshop perception.
