[![DOI](https://zenodo.org/badge/511911900.svg)](https://zenodo.org/doi/10.5281/zenodo.10948374)

# The GLAUx corpus

GLAUx (the Greek Language Automated) is a large corpus (currently 20M tokens) of Ancient Greek (currently 8th century BC - roughly 4th century AD), automatically annotated for morphology and syntax. This repository provides the raw data (in XML format), a queryable interface is present at https://glaux.be/.

## Data

The raw texts in GLAUx come from a number of public projects, including [Perseus](https://github.com/PerseusDL/canonical-greekLit), the [First1KGreek](https://github.com/OpenGreekAndLatin/First1KGreek) project, [Wikisource](https://el.wikisource.org/wiki/%CE%9A%CF%8D%CF%81%CE%B9%CE%B1_%CE%A3%CE%B5%CE%BB%CE%AF%CE%B4%CE%B1), and various other websites. For precise details, see the file metadata.txt.
Most of the data is available under a CC BY-SA license but some texts are more restrictive (e.g. CC BY-NC): the license of each source text is also specified in the metadata file.

**Note: the GLAUx corpus is encoded in Unicode-NFD, meaning that diacritics are separate characters (e.g. ά is two characters).**

## Annotation

At the moment GLAUx includes morphology, lemmas and syntactic dependencies, all roughly following the [Ancient Greek Dependency Treebanks](https://github.com/PerseusDL/treebank_data) guidelines. Part of GLAUx is manually annotated. These annotations come from various treebanking projects, which we thoroughly homogenized (see Keersmaekers et al. (2019): Creating, Enriching and Valorizing Treebanks of Ancient Greek for more details on this process):
* [The Ancient Greek Dependency Treebanks](https://github.com/PerseusDL/treebank_data), available under a CC BY-SA 3.0 license.
* [The PROIEL Treebank](https://github.com/proiel/proiel-treebank), available under a CC BY-NC-SA 3.0 license.
* [The Pedalion Trees](https://github.com/perseids-publications/pedalion-trees), available under a CC BY-SA 4.0 license.
* [The Gorman Trees](https://github.com/vgorman1/Greek-Dependency-Trees), available under a CC BY-NC-SA 4.0 license.
* [The Harrington Trees](https://github.com/perseids-publications/harrington-trees/), available under a CC BY-SA 4.0 license.
* [Treebank of Aphthonius' Progymnasmata](https://github.com/polinayordanova/Treebank-of-Aphtonius-Progymnasmata), no license specified.

All credits for the manual annotation belong to the respective projects.
These treebank projects have also been used as training material for the automatic annotation (most of GLAUx is automatically annotated). For details on the methodology, for lemmas and syntax the methodology is still roughly following the paper cited below. For morphology I currently use a transformer-based approach. The most recent code, including a reference to the paper describing the automated morphological analysis, can be found on https://github.com/alekkeersmaekers/glaux-nlp.

## The future of GLAUx

In the near future, the following steps will be taken in order to improve the quality of GLAUx:
* Adding more texts from later periods.
* Integrating the papyrus corpus available at https://github.com/alekkeersmaekers/duke-nlp.
* Improving the quality of the automatic annotation, in particular syntax.
* Adding more automatic annotations (in particular semantic annotation).

## Credits

The GLAUx corpus is the work of Alek Keersmaekers, with the help of various other people including Toon Van Hal, Wouter Mercelis and Mark Depauw. The online interface is developed by Frédéric Pietowski and Toon Van Hal. If you use either the online query interface or the raw data in your research, please refer to the following paper:
> Keersmaekers, Alek (2021): The GLAUx corpus: methodological issues in designing a long-term, diverse, multi-layered corpus of Ancient Greek. *Proceedings of the 2nd International Workshop on Computational Approaches to Historical Language Change 2021*, 39–50. Online: Association for Computational Linguistics. doi:10.18653/v1/2021.lchange-1.6.

We are grateful to the annotators of the various treebanks projects listed above, as well as the projects providing publicly available Greek texts, without which GLAUx could not exist.

GLAUx was funded by the Research Foundation - Flanders (FWO) through the following projects:
* *Corpus linguistics in the Greek papyri: developing a corpus to study variation and change in the post-classical Greek complementation system* (1162017N)
* *Towards a breakthrough in the automated parsing of Ancient Greek papyrological and literary texts? Extending and refining the available training data* (3H180705)
* *Language and Ideas: Towards a New Computational and Corpus-Based Approach to Ancient Greek Semantics and the History of Ideas* (3H200733)

## License

GLAUx is generally available under a [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license. Please note though that some of the texts and/or the manual annotations may have a more restrictive license.
