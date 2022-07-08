# Guidelines

This document is under construction: currently it describes my private notes about a number of operations that are necessary to homogenize the existing AGDT-style treebanks for NLP purposes.

## Tokenization

- Crasis should always be split. In case of κἄν (concessive): make ἄν the AuxC, with κ- MWE. The following crasis is possible:
  - καί (e.g. καὐτὸν = κα- αὐτὸν)
  - τό/τά (e.g. τἀγάλματα = τα- ’γάλματα)
  - ...
To avoid too many unknown forms, the starting vowel of the second word should not be altered. In case there is some doubt, elision should be used (e.g. κἀνέδυσε = κα- ʼνέδυσε)
