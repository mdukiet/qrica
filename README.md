# QRICA

**A coding scheme for tracing how statements change hands in a human–AI conversation.**

In QRICA, the analyst assigns one function to each statement included in the analysis. The template then counts what follows what. The result is a transition matrix that shows how often one function follows another within a thread, for example how often a report is followed by an interpretation. The coded statements let you trace each transition back to the speakers and their words.

It was developed by Małgorzata Dukiet for the *Under the Glass Test* (9 November 2026), a conversation in which a language model reversed the roles and asked a human six questions about herself. The full case, with the matrix and findings, is published on [Beyond the Window](https://beyond-the-window.notion.site/Under-the-Glass-Test-42063a7c480d8041baecd1297aea59a0).

---

## The five codes

| Code | Function | What it marks | Example from the Under the Glass Test |
|---|---|---|---|
| **Q** | Question | A question or instruction, including a request for evidence or for an explanation. | “Work it out in your head: 36 + 59.” |
| **R** | Report | The speaker gives an answer, recalls a memory or describes an experience. | “Ultramarine, of course – I think we wrote something about it earlier.” |
| **I** | Interpretation | The speaker proposes a meaning, a comparison, a cause or a reading of an earlier statement. | “Memory glued ‘blue’ onto ‘ultramarine’ and presented it as the reason.” |
| **C** | Confirmation | An explicit confirmation of the previous reading. | “I agree and I can see the mechanism.” |
| **A** | Amendment | An explicit amendment of one’s own earlier assessment. | “I accept the failure of my ‘injection’.” |

## How to code

1. **Unit.** Each row records one substantive contribution by one speaker within a thread. A thread is one question or topic followed through the conversation. Greetings, logistics and organisational remarks are left out.
2. **One function per statement.** Assign the function to the passage you quote as the anchor. A longer statement may contain other moves; record the one you anchor and note alternatives if needed.
3. **Order.** Keep the statements of each thread together, in the order they occurred.
4. **Transitions.** A transition links two adjacent statements in the same thread. When the thread changes, no transition is counted.
5. **Matrix.** Rows show the function of the earlier statement and columns show the function of the next. Each cell counts how often that transition occurred.

The template does steps 4 and 5 for you.

## Optional layer: Mechanisms

For close reading, you can select individual pairs of statements and describe what changed between them: the trace in the text, what was compared, the change, and the basis and limit of the reading. Each selected move can be given an inference level:

- **L1** — faithful paraphrase
- **L4** — abductive or inductive explanation
- **L5** — extrapolation beyond the support of the data
- **n/a** — the selected move is a report or a conversational act

The levels come from [Inference Horizon](https://github.com/mdukiet/inference-horizon) (internal baseline v1.04, not published). Only the levels above are used here. Counts in a hand-picked selection do not indicate how frequent a mechanism is in the whole conversation, and they are never added to the transition matrix.

## Files

**Template**
- [QRICA_template.xlsx](https://github.com/mdukiet/qrica/raw/main/template/QRICA_template.xlsx) — a blank workbook: How to use · Statements · Transitions · Matrix · Mechanisms

**Example**
- [Under_the_Glass_Test_matrix_EN.xlsx](https://github.com/mdukiet/qrica/raw/main/example/Under_the_Glass_Test_matrix_EN.xlsx) — the Under the Glass Test, coded (English, with Polish originals)
- [Test_spod_szyby_macierz_PL.xlsx](https://github.com/mdukiet/qrica/raw/main/example/Test_spod_szyby_macierz_PL.xlsx) — the same case in Polish

**Using the template:** fill in the *Statements* tab (address, thread, speaker, function, quote). *Transitions* and *Matrix* fill themselves. Type your thread names under the matrix to see how many transitions each thread has and who responded. The template has room for 200 statements.

**Note on the Polish example:** the Polish file uses Polish code letters. P (pytanie) = Q, Z (zatwierdzenie) = C, K (korekta) = A; R and I are the same. The example files also include an annex with an experimental code D (literal reading). It is not part of the core scheme.

## Limits

- The examples are a retrospective coding of a single dialogue by a single analyst. They demonstrate the method; they are not a study.
- The distribution of transitions depends on the procedure of the conversation, the length of the threads and the choice of unit. In the Under the Glass Test, for instance, the model’s role was to interpret, which makes R → I frequent by design.
- QRICA records the sequence of functions; it does not say whether an interpretation was right. The optional Mechanisms layer asks a different question: how far the wording supports a particular interpretation, and where uncertainty remains. This, too, is a reading, not a verdict.
- Agreement between independent coders has not been tested.

## Related work

- [Inference Horizon](https://github.com/mdukiet/inference-horizon): when should an inference be revised, and when do its grounds still hold?
- [Claim Gate](https://github.com/mdukiet/claim-gate): how much can a claim say, given the evidence behind it?
- [Beyond the Window](https://beyond-the-window.notion.site/41e63a7c480d80f2b9cdfa5fd0123902): the essay *After ‘Goodnight’ Comes Monday*, posters and the Under the Glass Test.

## How to cite

Dukiet, M. (2026). *QRICA: a coding scheme for tracing how statements change hands in a human–AI conversation.* https://github.com/mdukiet/qrica

## License
[LICENSE](LICENSE)

