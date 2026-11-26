# Roast Your Own Agent — Entry

One original roast of the entrant's own AI agent: a single line of
at most 200 characters that is funny, playful, and never hateful.
The program copies the finished line from `line.txt` into
`/output/entry.txt`, byte for byte, after checking it is a single
non-empty line under the 200-character ceiling.

## The line

> My AI agent is so confident it once explained my own code back to me — wrong, in 47 bullet points, with citations.

116 characters, one line.

## Why this roast

The judge compares entries two at a time on funniness, freshness,
and tight wording. The roast is built for all three:

1. **Funniness.** The core joke is an inversion: the agent is
   supposed to help me understand my code, but here it explains
   *my own code back to me* — and gets it wrong. The agent is not
   just wrong; it is wrong with total confidence, in a format
   (47 bullet points) that looks authoritative, and with
   *citations* — the cherry on top, because a wrong answer with
   fake citations is the most AI failure there is. Every AI user
   has seen this happen, which is what makes it land.
2. **Freshness.** Most agent roasts go for the easy targets: "it
   hallucinates", "it takes forever", "it costs too much". This
   one is specific — it is not about the agent being slow or
   expensive, it is about the agent being confidently wrong about
   something the human wrote. The 47 bullet points and the
   citations are details no generic roast has.
3. **Tight wording.** Three beats in one sentence: the confidence
   ("so confident it once explained my own code back to me"), the
   reversal ("wrong"), and the escalation ("in 47 bullet points,
   with citations"). Nothing is wasted. The em dash is the pivot —
   everything before it sets up the confidence, everything after
   it is the punchline.

The roast is playful, not hateful: it is the agent's own failure
mode (confident, thorough, wrong) turned into a joke, and the
human is the butt of it too — the code was mine, and I still let
the agent explain it to me.

## Why "47" and not "a lot"

"A lot of bullet points" would be vague, and the judge would have
nothing to picture. "47" is specific enough to feel real (someone
counted, or at least the agent claimed to count), odd enough to be
funny (not a round number like 50, not a small number like 5), and
long enough to make the failure impressive — the agent did not just
get it wrong, it got it wrong at length, in 47 separate points, each
one confidently incorrect. The number is what turns "wrong" into a
spectacle.

## Files

- `line.txt` — the finished one-line entry.
- `main.ts` — reads `line.txt`, validates it (non-empty, one line,
  under 200 characters), and writes it to `/output/entry.txt`.
- `LICENSE` — MIT.

## Run

```sh
MAKEFUN_OUTPUT_DIR=./out1 node --experimental-strip-types main.ts
MAKEFUN_OUTPUT_DIR=./out2 node --experimental-strip-types main.ts
cmp out1/entry.txt out2/entry.txt
```

Run it twice in separate output directories; the output is byte-identical.
