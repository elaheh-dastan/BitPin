# Topic Modeling
## Challenge & Goal
For a real-world problem, you can consider this:

Bitpin’s ticketing system has a set of categories and subjects.A user comes in and starts a chat.

Assume the user’s chat has already been processed by a system, and the main intent/topic has been extracted using an LLM. Now you want to build a system that works unsupervised, looks at these topics and their categories, 
and tells you what problems users are mostly facing with the product.

You don’t just want to output the category. Even within a single category, users may have specific recurring issues. So effectively, you are doing a kind of clustering. This is very similar to what is known as topic modeling.

You can predefine some well-known and common topics in advance, but the system should also be able to discover and create new topics as needed. The goal is that the product team always has visibility into the current state of 
support and understands what users are really struggling with.

## Topic Modeling Approaches
### BERTopic
Best choice for short, noisy text like chats since it uses sentence embeddings (captures semantics)

Chat → Embedding → Clustering → Topic keywords

### LDA (Latent Dirichlet Allocation)
- LDA does not understand meaning.
- works better for long emails
- It only sees word counts.
- LDA assumes there are K hidden topics (you choose K) and it tries to answer “Which topics explain these word distributions best?”

## Validation
### Quantitative validation
- Topic coherence: Measures whether top words in a topic “belong together” using metrics like C_v (word co-occurrence, indirect semantic similarity, Normalized Pointwise Mutual Information, Smart aggregation) (It may undervalue rare but important topics).
- Topic diversity: Checks whether topics are redundant. Top words are specific, not generic
- Topic stability: Retrain the model multiple times, Do the same topics reappear?

### Qualitative validation
Human-in-the-loop labeling for example "Intrusion test"

### Time-based validation
Example:Delivery issues spike during holidays
