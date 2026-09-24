# Subjectivity Space

**Continuous representations for modelling ambiguity in subjective language**

MSc Computer Science (Artificial Intelligence: Speech & Language Processing)  
University of Sheffield

This repository contains experimental code developed as part of my MSc research into **Subjectivity Space**: a neural-network approach for representing subjective language using continuous multidimensional coordinates rather than relying exclusively on rigid categorical labels.

The project developed from earlier **Intent Space** research and adapts the underlying continuous-space idea to subjective language, with hate-speech detection used as the primary experimental domain.

## Research Motivation

Subjective language is often difficult to represent using a single discrete label. Different annotators may interpret the same sentence differently, and apparently conflicting annotations can contain meaningful information rather than simply noise.

Subjectivity Space investigates whether multiple subjective characteristics can instead be represented as coordinates within a shared continuous space.

The research involved:

- designing a continuous-coordinate NLP task;
- adapting and extending an existing neural-network research model;
- constructing a corpus from ten heterogeneous hate-speech datasets;
- neural sequence modelling using word embeddings and recurrent neural networks;
- experiments involving limited-data and unseen-category generalisation;
- model-stability improvements;
- comparison with a baseline RNN; and
- human evaluation of model predictions.

## Results

The enhanced Subjectivity Space system achieved a **peak accuracy of 83.5%**, compared with **50.2% for the baseline RNN** in the experimental evaluation.

The work also investigated whether continuous representations could support generalisation when categories were unseen or training data were limited.

## Repository Structure

The repository contains experimental code from different stages of the research programme. Some directory names retain terminology from the earlier **Intent Space** implementation from which Subjectivity Space developed.

### `main`
Core continuous-space training experiments.

### `limited_data`
Experiments training models with restricted quantities of labelled training data.

### `leave_one_out`
Leave-one-out experiments investigating generalisation to unseen categories.

### `main_2unseen`
Experiments involving unseen-category conditions.

### `Experiment-3-grid-search`
Hyperparameter-search experiments.

### `RNN`
Baseline recurrent neural-network experiments used for comparison.

### `ATIS`
Earlier experiments using the ATIS intent-classification dataset.

### `Create-dataset`
Dataset construction and preparation utilities.

### `precision-recall-curve`
Evaluation and precision/recall analysis.

### `euclidean`
Experiments involving distance-based calculations within the continuous representation space.

## Data

The Subjectivity Space experiments used a corpus constructed by integrating and preprocessing **ten hate-speech datasets**.

The associated dataset-engineering work is maintained separately as:

**Corpus of Hate Speech from Ten Datasets**

This involved cleaning, preprocessing and integrating heterogeneous sources into a resource suitable for neural sequence modelling and experiments involving ambiguous and overlapping subjective categories.

## Technical Approach

The research explored:

- Python
- recurrent neural networks
- Elman-type RNN architectures
- word embeddings
- GloVe representations
- continuous multidimensional representations
- Layer Normalisation
- Mish activation
- gradient clipping
- grid search
- limited-data experiments
- leave-one-out evaluation
- model stability
- human evaluation
- Cohen's Kappa

## Human Evaluation

In addition to intrinsic model evaluation, the project included a human user study examining the relationship between model predictions and human perception.

Participants completed three annotation tasks, and model-human agreement was evaluated using **Cohen's Kappa**.

This provided an extrinsic evaluation of whether the continuous representations captured distinctions that were meaningful to human annotators.

## Research Contribution

The project explored a broader question in human-centred NLP:

> Can disagreement and ambiguity in subjective language be represented as useful structure rather than treated solely as classification error?

Subjectivity Space approaches this by representing subjective characteristics continuously and allowing multiple characteristics to coexist within the same representation.

## Related Project

The ten-dataset corpus and preprocessing pipeline are available as a separate GitHub project and form the data-engineering component of this research.

## Author

**Monika Wiczewa**  
Creative Technologist | AI/ML | NLP & Human-Centred AI | Music Technology

MSc Computer Science (Artificial Intelligence: Speech & Language Processing), Distinction  
University of Sheffield

[LinkedIn](https://www.linkedin.com/in/monika-wiczewa-9771771a3/)
