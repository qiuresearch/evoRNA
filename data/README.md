## Description of data

For files not in the github data folder, please visit the shared Google drive @  https://drive.google.com/drive/folders/1QlC8I1XqEG-v6QlMcn7X9XAVKNDnlNS9?usp=sharing

### metafam2d_nr80.pkl (here) and metafam2d.pkl (in the google drive above)
Files are pickled Pandas dataframes that be read in via "pd.read_pickle()". Dataframes contain a number of metadata columns describing the features/statistics of each sample. 

The columns most relevant to RNA secondary structures are:

* "idx": the unique index for each sample
* "id": idx and the original file name
* "seq": RNA sequence (i.e., AUGC)
* "moltype": RNA biological type
* "dbn": RNA secondary structure in [dot-bracket notation](https://gensoft.pasteur.fr/docs/ViennaRNA/2.4.14/rna_structure_notations.html#:~:text=and%20Conversion%20API-,Representations%20of%20Secondary%20Structures,bases%20are%20shown%20as%20dots.)
* "ct": RNA secondary structure as [connectivity table](https://rna.urmc.rochester.edu/Text/File_Formats.html).

Note that both "dbn" and "ct" formats can be converted into a contact/adjacency matrix. The task of strucutre prediction is to output the contact matrix with sequence as the input.

### metafam2d.rnaforester.dbnIdentity_pairwise.pkl
The pairwise similarity matrix obtained by RNAforester. The columns and indices are the "id"s as in metafam2d.pkl.