# Security and safety

ako has two kinds of safety to take seriously, and they are not the same thing.

## Physical safety comes first

ako is a teaching aid, not a safety device. It coaches, warns, and verifies, but it has
no connection to the machine and cannot stop it. **Never rely on ako to keep you safe at
a lathe.** Only the operator controls a manual lathe, and all the usual precautions,
guarding, training, supervision, and the machine's own stops, remain the operator's
responsibility in full. ako is designed to fail safe (when unsure, it asks the human and
withholds approval), and that design is a backstop, not a guarantee.

If you find a way the design could lull a learner into an unsafe action, that is exactly
the kind of report we want. Raise it as an [issue][issues] or, if you would rather not do
so publicly, through the private channel below.

[issues]: https://github.com/vernonkay/ako/issues

## Software vulnerabilities

ako is pre-software at the idea stage, so there is little attack surface yet. Once there
is code, this is how to report:

Please report security issues **privately**, not in a public issue. Use GitHub's private
vulnerability reporting: the repository's **Security** tab, then **Report a
vulnerability**. That opens a confidential channel with the maintainer. Include what you
found, how to reproduce it, and the impact as you see it. You will get an acknowledgement,
and a fix or an explanation once it has been assessed.

## When there is a product

A camera and microphone pointed at a person in a workshop is sensitive by nature. As the
software takes shape, the threat model we will hold ourselves to: keep as much perception
on the machine as possible, be explicit about anything recorded or sent off-device, and
treat a learner's footage as theirs. Reports and design critique in this area are
especially welcome.
