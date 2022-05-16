# NLP Workshop

Hi, this is my NLP workshop on Pre-training, Metrics, and Community!
It was designed for a 3-hour block at ML Prague.

The workshop is in English, but encourages attendees to explore Czech-language data and models.
I believe that this part of the workshop is adaptable for other languages.

The workshop assumes knowledge of Python and pip. If students have done fine-tuning
before, this could be a little easy. I would encourage these
students to try a new library or read the docs to try something new.

The public notebooks are incomplete. I have a "cheat" folder with solutions, so I
know the problems are solvable and I can check if there is a problem.

## Part 0: Slides

Initial explanation and discussion:
- Speaker and Agenda intro
- What do we mean by Pre-Trained Models, do they represent general reality
- Metrics used to back ML as an objective science
- What we choose to optimize, label shift over time, learning in a toxic language environment.
- Tech discussion groups, model sharing

Link: https://docs.google.com/presentation/d/1HL7ryS60yyj5Mo9x1JMojts6lu68KyRJuPpCTM4UQ0s/edit?usp=sharing

## Part 1: Movies

Goals: fine-tuning, frozen layers, and adapter

Given a local language movie review dataset,

- Explore dataset and make choices (classification or regression? train/test split? include movie name?)
- Choose a recommended model
- Choose a library (notebooks available for Transformers, SimpleTransformers, AdapterHub)
- (Advanced) add metrics, choose an optimizer, explore other options

**The choices are real. There is more than one answer.** It is easier to classify
positive vs. negative or do regression vs. making each star rating 1-5 a class.
If we include movie names then it might improve accuracy now, but less so on future movies.

### Report back to Group

I advise taking a .sample(10_000) of the dataset and running for only one epoch so it
takes ~15 minutes to train.

During training, write a README to report back to group:

- How did you prepare your data and model?
- What info did you see *during* training?
- What was your accuracy on the test dataset?
- What advice do you give to someone repeating your experiment or re-using your model?

## Part 1B: Sharing the model

Slides: what is the HuggingFace model hub, filter options, interactive parts.

Goals: Share your current model on HuggingFace or AdapterHub. After the workshop you can
train more and then `git push` your updated model.

- Complete training and README
- HF: notebook_login() / push_to_hub(model_name)
- AdapterHub: read docs on how to make a Pull Request

## Part 2: GPT

Slides: Completing sentences, adding context. Using countries or gender cues to change
GPT's expectations.

Goals: Understand next-token probabilities.

- Create interesting sentences with local language GPT
- Use ECCO to visualize token probabilities
- Different languages prompt differently (Spanish el/la un/una)

## Part 2B: Decoders

Goals: Understand different ways to sample from probabilities.

- Compare results with typical decoding
- Options for beam search, etc.

## Part 3A: Least time permitting, ROME

- Insert tokens into GPT
- Edit factual knowledge (ROME, https://github.com/kmeng01/rome)

## Part 3B: Most time permitting, QA / SQuAD / ColBERT

- Explain a SQuAD dataset exists
- Explain semantic search vs. full text search
- Give a demo of training ColBERT, adding docs
