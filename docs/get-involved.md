# Get involved

ako is at the idea stage, which is the best time to shape it. These are the open questions
we most want help on. Pick any one and come to
[Discussions](https://github.com/vernonkay/ako/discussions), or open an
[issue](https://github.com/vernonkay/ako/issues) if it is concrete.

## If you teach or run a lathe

- **The certification.** What would you insist a beginner prove before you let them cut?
  What have we missed in a camera-verifiable machine-control gate?
- **The dangerous moments.** What are the near-misses and the real injuries you have seen,
  and which could a camera have caught in time?
- **The curriculum.** There is no open lathe curriculum. What order did you learn in, or
  teach in, and what is the smallest first project that teaches the most?
- **The "you work it out" moments.** Where is it right for a tutor to hand the thinking
  back to the learner rather than give the answer?

## If you build realtime or on-device AI

- **The backbone.** We lean toward building on an open realtime voice-and-vision framework
  (Stream's Vision Agents is the current first choice, with heavier WebRTC-native options
  as fallbacks). Where is that naive? What would you choose?
- **Perception feasibility.** How reliably can today's models tell a glove from a bare
  hand, see a chuck key in the chuck, judge the spindle stopped, or read a digital readout,
  at useful latency and cost? What is realistic, and what is wishful?
- **Audio.** Telling a clean cut from chatter and recovering spindle speed from sound looks
  like cheap, high-value signal. Has anyone done this well?

## If you care about safety and ethics

- **The fail-safe stance.** Is "coach, never control, and defer to the human on
  uncertainty" the right line? Where could the design still lull someone into an unsafe
  action?
- **Privacy.** A camera on a person in a workshop is sensitive. What should the defaults
  be for what is kept, and what should never leave the machine?

## A housekeeping question

- **Licensing of the written material.** Code is dual MIT OR Apache-2.0. Should the prose
  in `docs/` be CC-BY-4.0 instead, which fits written work better? Views welcome.

You do not need permission to start a Discussion, and there is no contribution too small,
a correction, a reference, a war story. Every post gets a reply, see
[`../TRIAGE.md`](../TRIAGE.md).
