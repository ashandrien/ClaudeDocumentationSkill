# Code comments

Comments explain what isn't obvious from the code itself:
- Why an unusual decision exists.
- Business rules that are not obvious.
- Limitations of external systems (an API, a database, a cloud service).
- Workarounds.
- Non-obvious performance decisions.
- Important assumptions.

Prefer clear code over explanatory comments. Skip comments that translate code into English:

```python
# Loop through users
for user in users:
```

Don't comment every function or block to make the code look documented.

## Leave the conversation out of comments

A comment describes the code as it is. It never records the conversation, session, review or request
that produced the code. Don't write comments like these:

```python
# Added per review feedback
# Changed from a list to a set, as discussed
# Now retries three times (was once)
# Fixed the bug where the queue name was empty
# As requested, this skips archived accounts
# Previously this called get_account() directly
```

If the reason behind a decision still matters to a future reader, state the reason itself ("the billing
API drops the connection after 30 s, so the export retries"), not how you arrived at it. The history
belongs in the commit message or PR description.

Also leave out comments about how the code was generated or edited.
