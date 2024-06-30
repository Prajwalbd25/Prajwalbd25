def amino_acid_composition_mod(amino_acid_seq):
    amino_acid_seq = amino_acid_seq.upper()
    amino_acids = {
        "A": 0,
        "C": 0,
        "D": 0,
        "E": 0,
        "F": 0,
        "G": 0,
        "H": 0,
        "I": 0,
        "K": 0,
        "L": 0,
        "M": 0,
        "N": 0,
        "P": 0,
        "Q": 0,
        "R": 0,
        "S": 0,
        "T": 0,
        "V": 0,
        "W": 0,
        "Y": 0
    }

    for hehe in amino_acid_seq:
        if hehe in amino_acids:
            amino_acids[hehe] += 1
        else:
            print("unexpected character encountered")
    return amino_acids

import re
amino_seq_clean = re.compile("\n")
from module import amino_acid_composition_mod

with open("P06213.fasta", "r") as amino_fasta:
    aino_fasta.readline()
    amino_full_seq = amino_fasta.read()
amino_seq_cleaned = amino_seq_clean.sub("", amino_full_seq)
print(amino_acid_composition_mod(amino_seq_cleaned))


