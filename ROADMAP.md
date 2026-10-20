# Roadmap

ako is at the idea stage. This is the outward-facing plan, and it will move as the idea
is pressure-tested. Nothing here is a commitment to a date. Ideas and priorities are
welcome, open an issue or come to [Discussions](https://github.com/vernonkay/ako/discussions).

The plan is deliberately staged so that the hard, distinctive parts are proven small
before anything is built wide.

## Now, the idea made concrete

The goal of this stage is to turn a conviction into things people can argue with.

- **The idea, written down** (this repository): vision, concept, the three commitments,
  and the open questions.
- **A camera-verifiable machine-control certification (Level 0).** The first concrete
  design: a scored, observed sequence that proves a learner knows their stops, can stop
  on command, and keeps clear, before any cutting is unlocked. This is where ako's
  safety-first stance becomes a real mechanism rather than a slogan.
- **One guided project (Level 1), end to end.** Facing and turning a simple part, as the
  worked example of the guided-project format: steps, skills, hazards, mastery checks,
  and the moments where ako says "you measure that and tell me".
- **Prove the riskiest perception on a real machine.** A focused spike on the
  safety-relevant things only: is the chuck key in, is a glove or sleeve present, is the
  spindle turning, does the sound say the cut is clean or chattering. Feasibility,
  latency, and cost, before anything depends on them.

## Next, the format and the perception layer

- **The guided-project format and the skill ladder.** A stable novice-to-skilled
  progression (safety, turning, drilling, tapers and knurls, boring and reaming,
  threading, precision) that projects slot into.
- **Perception on open building blocks.** Hand and pose detection, machine registration
  with fiducial markers, reading a digital readout, and chatter-from-sound, assembled
  from existing permissively licensed components rather than built from nothing.
- **A graduated instrumentation path.** Camera-only must always work, because asking a
  beginner to instrument a machine is itself a barrier. Optional low-cost add-ons (a
  self-ejecting chuck key, a tachometer, markers) make the machine safer and easier to
  read, and are framed as a reward, never a toll.

## Later, and under consideration

Tagged speculative so they cannot quietly block the shippable core. Each would need its
own exit criteria before it is taken seriously.

- **Spatial grounding** (cut depth, centre height, diameter off spinning work). The
  hardest perception problem, and the one most likely to stay a "you work it out and tell
  me" moment for a long time.
- **A hands-free form factor** (smart glasses or a fixed rig) once the fixed-camera
  version earns it.
- **Community-authored projects and multiple machines**, once the format is proven on
  one.

## What we expect to stand on

From an open-source prior-art scan, ako is a genuine new-start project rather than a fork:
no existing project combines the manual-machining domain, the coach-never-controls safety
stance, and a graded realtime see-and-coach loop. But the plumbing is a solved problem, so
we build on it:

- A **realtime voice-and-vision framework** as the backbone (current first choice: Stream's
  Apache-2.0 Vision Agents, which already pairs realtime voice with pose tracking for
  coaching; heavier WebRTC-native alternatives exist as fallbacks).
- **MediaPipe** (Apache-2.0) for hands and pose, **AprilTag / ArUco** for registering the
  machine in frame, and a purpose-built audio layer for chatter and spindle speed.

The ground that is genuinely ours to make: the safety-first coaching contract, the lathe
curriculum (there is no open one), and perception tuned to a workshop. That combination,
not any single component, is why ako is a new start.
