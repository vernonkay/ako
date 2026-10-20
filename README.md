# ako

**An AI tutor that sits beside you at a manual lathe, watches, and teaches you to run
it safely.**

Point a camera and a microphone at a real engineering lathe. ako watches what you do,
talks you through a project step by step, checks your technique, and coaches you from
your first safe start-up to real turned parts. One learner, one machine, one patient
teacher that never looks away.

> **ako** is te reo Māori for *to learn, and to teach*. One word for both, because good
> instruction is a relationship, not a broadcast.

## This is an idea, not software (yet)

ako is at the idea stage, and this repository is the invitation. There is nothing to
download. What is here is the thinking: what ako is, why it is worth building, the hard
problems, and where you can help shape it before a line of the product is written. If the
idea pulls at you, whether you run a lathe, teach in a workshop, or build realtime AI,
this is the moment to come in.

Start with **[VISION.md](VISION.md)** for the north star and the deliberate non-goals,
**[docs/concept.md](docs/concept.md)** for how a session actually works, and
**[ROADMAP.md](ROADMAP.md)** for the path from idea to something you can stand at a
machine and use.

## Why it matters

Learning a manual lathe is a doorway into the machining trades, and the doorway is
narrowing. The people who teach it are retiring, night classes are closing, and a lathe
does not forgive: a chuck key left in, a dangling sleeve, or a hand reaching toward
spinning work can cost a finger or worse. A beginner alone with a lathe and a video
playlist has no one beside them to say "stop, not like that". ako is built to be that
someone.

## The three commitments

These are the spine of the project, and the first non-goals in the vision exist to
defend them:

- **It coaches, it never controls.** ako has no wires to the machine and no power to stop
  it. Only the human stops a manual lathe. ako watches, warns, verifies, and withholds
  approval, and it fails safe: when it is not sure, it says so and asks the human. It
  never decides for you that you are safe.
- **The operator stays the thinker.** Where ako cannot reliably see something, it does
  not pretend to. It asks you to measure it, work it out, and report back. That is honest
  engineering and better teaching than a confident guess.
- **Safety is the first thing you learn, and it is checked.** Before ako unlocks any
  cutting, you pass a camera-verified machine-control certification: knowing your stops,
  proving you can stop on command, keeping clear. A camera can be the patient observer
  that a workshop checkout usually needs a human for.

## Where this is going

Private for now while the idea takes shape, public once there is enough to rally around.
The near-term plan is to build on an existing open-source realtime voice-and-vision
framework rather than from scratch, and to own the parts that exist nowhere yet: the
safety-first coaching contract, the lathe curriculum, and perception that can read a
workshop. See [ROADMAP.md](ROADMAP.md).

## Get involved

- **Ideas, questions, how you teach or learn this** come to [Discussions][discussions].
- **A concrete proposal or a problem to track** open an [issue][issues].
- [`docs/get-involved.md`](docs/get-involved.md) lists the open questions we most want
  help on, and [`CONTRIBUTING.md`](CONTRIBUTING.md) and
  [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) set out how we work.

[discussions]: https://github.com/vernonkay/ako/discussions
[issues]: https://github.com/vernonkay/ako/issues

## Licence

Dual-licensed under **MIT OR Apache-2.0**, at your option. See
[`LICENSE-MIT`](LICENSE-MIT) and [`LICENSE-APACHE`](LICENSE-APACHE). The written material
in `docs/` may move to CC-BY-4.0; that is still open, see
[`docs/get-involved.md`](docs/get-involved.md).

## Built with AI assistance

ako is created by Vernon Kay with heavy use of AI assistance (Claude Code). The
decisions and the responsibility are the author's; the AI is a tool, disclosed here
rather than credited per commit.
