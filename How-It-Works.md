# The Chain

Mentalist generates wordlists by linking together **nodes**, which form a **chain**. The first node in a chain is always the **Base Words** node. When the chain is processed, each Base Word passes to the next node in the chain, which might modify the word, leave it the same or create more variations of it. Finally, the results are written to an output file as either the full wordlist or rules to generate the equivalent list.

# Nodes

There are 5 types of nodes. Each type has its own set of attributes, which can be added in any combination. A node's attributes determine its function. Furthermore, _attributes within the same node are mutually exclusive from each other_.

Some nodes may produce more than one output word for each input word. In such cases, only the set of unique output words for a Base Word is passed on to the next node. In other words, _each node performs de-duplication on each base word_.

|Type|Description|
|----|-----------|
| Base Words |  Always the first node within the Mentalist chain. It provides the root words, which are to be processed by each node as they pass down the chain. |
| Case | Changes the case of letters within the word. Each attribute added to a Case node produces a different variation of the input word, except for the No Case Change attribute which passes through the original word. |
| Substitution | Replaces characters within the word. Like Case, each attribute added to a Substitution node produces another output word, subject to de-duplication. The No Substitution attribute gives the unmodified input word. |
| Append | Append nodes add strings to the end of the input word. Most Append attributes produce many variations of the input word. For example, the `Numbers: Small (0-100)` attribute adds 101 output words for each input word. |
| Prepend | Prepend nodes add strings to the beginning of the input word. Its attributes and functionality is otherwise identical to Append. |

# Attributes

Each node has the ability to perform one or more actions on the input words. These actions are specified in each node's attributes. Attributes within the same node are _mutually exclusive of each other_ and, as a consequence, a node can have no duplicate attributes.

Further information on nodes' unique attributes can be found in the [Node Attributes](https://github.com/sc0tfree/mentalist/wiki/Node-Attributes) section.