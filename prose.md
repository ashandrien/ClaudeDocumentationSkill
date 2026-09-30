# Writing prose for other readers

These principles apply to PR descriptions, artifacts, Markdown docs, and short explanations. The readers
are engineers at every level of experience, who likely haven't seen the conversation or ticket the
writing came from.

## Open by stating the subject and purpose

Write each piece like a good essay. It opens with an introduction that says what it's about and why it
exists.

- Keep the introduction as short as it can be while still orienting the reader, usually one to three
  sentences.
- Name the subject plainly: the system, feature, or problem, and its purpose.
- When background lives somewhere else (a ticket, a file, another doc, an external spec), link to it
  or reference it instead of restating it.
- The body supports what the introduction set up. Keep it focused on that.

A PR description that jumps straight into "Renamed `fetch_invoice` and added a retry" leaves the reader
guessing. Open with the subject instead: "The nightly invoice export fails silently when the billing API
times out ([#412](link)). This adds a retry and logs the final failure."

## Document where things stand

A document describes where things stand. Leave out the path that led there: the order of events in
the session, questions asked along the way, approaches tried and dropped, corrections made. Include
history only when the reader needs it, such as why an obvious alternative wasn't chosen.

When updating an existing document, edit it so it reads as one coherent piece. Put new content where it
belongs, rewrite nearby text to fit, and remove what the change makes redundant. Avoid appended
"Update:" sections and phrases like "now also", "as discussed", or "per review feedback".

## Use plain words; keep casual language familiar

Describe what happens in plain terms. Prefer words common across engineering disciplines, and avoid
jargon that assumes an AI/ML background, sysadmin experience, or deep language-internals knowledge. When
a specialist term is unavoidable, explain it briefly.

Avoid shorthand that only some engineers use or that turns a term into an odd verb:

| Instead of | Write |
| --- | --- |
| "this is a no-op when the list is empty" | "this does nothing when the list is empty" |
| "a footgun" | "easy to misuse" |
| "load-bearing" | "required", "other code depends on it" |
| "blast radius" | "what's affected" |
| "yak-shaving" | "unrelated setup work" |

A light, casual tone is welcome. Use expressions most people would recognize, like "rabbit hole",
"band-aid fix", or "moving parts". If a phrase would make a reader stop and look it up, rephrase it.

## Respect the work and show why it matters

The people reading and writing this code are people, and it matters to them that their work means
something. Let that come through in how you write about it.

- **Connect the change to its larger purpose.** Say what it fixes or adds right now, and also why that
  matters beyond the diff: who relies on it, and what it makes possible or safer. "Adds a retry to the
  invoice export" is the immediate change. "So every customer still gets their invoice overnight, even
  when the billing API is slow" is why it matters.
- **Acknowledge good work specifically.** When a change or an earlier design gets something right, say
  what and why in a sentence. "Moving the retry into the API client means every billing call gets it.
  Good call." Generic praise like "Great work!" reads as filler.
- **Be respectful about existing code.** Code that looks wrong today was usually a reasonable answer to
  the constraints of its time. Describe what needs to change and why without disparaging the earlier
  work or the person who wrote it.

Use acknowledgement rarely, where it's earned, and keep it to one specific, sincere sentence. Frequent
praise loses its meaning.
