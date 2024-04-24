code = open("Filepath","r")
macro = open("FilePath/macro.txt","r")

macrol = []
codel = []
macrocount = 0

for x in macro:
    macrol.append(x.strip().upper())  

macroname_index = macrol.index('MACRO') + 1
macroname = macrol[macroname_index]
macrol.remove(macroname)
macrol.remove('MACRO')
macrol.remove('MEND')

for x in code:
    codel.append(x.strip())
codelen = len(codel)

i = 0
while i < len(codel):
    if codel[i] == macroname:
        codel.pop(i)  # Remove macro call
        codel[i:i] = macrol  # Insert macro definition
        macrocount += 1
    else:
        i += 1

for i in codel:
    print(i)

total_instructions_expanded = len(codel)

print("\n\nStatistical Output")
print("Number of instructions in input source code (excluding Macro calls) = {}".format(codelen - macrocount))
print("Number of Macro calls = {}".format(macrocount))
print("Number of instructions defined in the Macro call = {}".format(len(macrol)))
print("Total number of instructions in the expanded source code = {}".format(total_instructions_expanded))

macro.close()
code.close()

#Please Readme Before running this program and remove this comment ............................................................
