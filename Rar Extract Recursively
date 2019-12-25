# Rar extract recursively , By EdbR
import os
from pyunpack import Archive
rarpath=r"Your path to directory of the first Rar"

while(1):
    FilesNames = os.listdir(rarpath)
    for name in FilesNames:
        Reverse = name[::-1]
        if (Reverse[0:3] != "rar"):                      # We want to check if the file already a rar.
            rar = rarpath + '\\' + name
            with open(rar, "rb") as f:
                x = f.read()
                print(chr(x[-2]) + chr(x[-1]), end="")   # The operation you need to do with the bytes.
                Archive(rar).extractall(rarpath)         # Extract the rar.
            os.rename(rar, rar + ".rar")                 # Make the file to rar.
        else:
            FileToDelete = rarpath + '\\' + name         # Rar that already used will remove to prevent name collision
            os.remove(FileToDelete)
            FileToDelete=rarpath
        rar = rarpath
