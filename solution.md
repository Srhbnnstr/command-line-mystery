```zsh
# Clone the initial repository
git clone git@github.com:eerwitt/command-line-mystery.git
cd command-line-mystery

# Check the status to see if anything is already marked as new (shouldn't be)
git status

# Edit my solution file
subl solution.md

# Commit initial solution
git add solution.md
git commit -a

# Start reading the instructions
less instructions

# Check for clues in the mystery
cd mystery
grep CLUE ./crimescene

# Search for person with the Latte
grep Annabel ./people

# Knock on her door
less streets/Mattapan_Street
# Goto line in file using less: http://stackoverflow.com/questions/8586648/going-to-a-specific-line-number-using-less-in-unix
# in less type 173g
# Try different interviews
less interviews/interview-47246024

less interviews/interview-699607

# Checking for vehicle
less vehicles
# Search in less for vehicles starting with L337 and ending in 9
# in less /L337..9
# Check which are over 6'
# Katie Park
# Mike Bostock
# John Keefe
# Erika Owens
# Matt Waite
# Brian Boyer
# Al Shaw
# Miranda Mulligan
# Joe Germuska
# Jeremy Bowers
# Jacqui Maher

# Check which is male/female and get their names
egrep '((Katie Park)|(Mike Bostock)|(John Keefe)|(Erika Owens)|(Matt Waite)|(Brian Boyer)|(Al Shaw)|(Miranda Mulligan)|(Joe Germuska)|(Jeremy Bowers)|(Jacqui Maher))' ./people | grep '\tM\t' | cut -f1

# Limit down by membership
egrep -R '((Joe Germuska)|(Brian Boyer)|(Mike Bostock)|(Jeremy Bowers)|(John Keefe)|(Al Shaw)|(Matt Waite))' ./memberships

# (Jeremy Bowers)|(Brian Boyer)|(Mike Bostock)|(Matt Waite)
# Not MB, wrong car color
# Not MW, wrong car manufacturer
# Not BB, wrong car manufacturer
# JB, it is JB
```

Sarahs-MacBook-Pro:~ sarah$ cd wdi
Sarahs-MacBook-Pro:wdi sarah$ cd command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ ls
cheatsheet.md	hint2		hint4		hint6		hint8		mystery		solution.md
hint1		hint3		hint5		hint7		instructions	readme.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd cat instructions
-bash: cd: cat: No such file or directory
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat instructions
.OOOOOOOOOOOOOOO @@                                   @@ OOOOOOOOOOOOOOOO.
OOOOOOOOOOOOOOOO @@                                    @@ OOOOOOOOOOOOOOOO
OOOOOOOOOO'''''' @@                                    @@ ```````OOOOOOOOO
OOOOO'' aaa@@@@@@@@@@@@@@@@@@@@"""                   """""""""@@aaaa `OOOO
OOOOO,""""@@@@@@@@@@@@@@""""                                     a@"" OOOA
OOOOOOOOOoooooo,                                            |OOoooooOOOOOS
OOOOOOOOOOOOOOOOo,                                          |OOOOOOOOOOOOC
OOOOOOOOOOOOOOOOOO                                         ,|OOOOOOOOOOOOI
OOOOOOOOOOOOOOOOOO @          THE                          |OOOOOOOOOOOOOI
OOOOOOOOOOOOOOOOO'@           COMMAND                      OOOOOOOOOOOOOOb
OOOOOOOOOOOOOOO'a'            LINE                         |OOOOOOOOOOOOOy
OOOOOOOOOOOOOO''              MURDERS                      aa`OOOOOOOOOOOP
OOOOOOOOOOOOOOb,..                                          `@aa``OOOOOOOh
OOOOOOOOOOOOOOOOOOo                                           `@@@aa OOOOo
OOOOOOOOOOOOOOOOOOO|                                             @@@ OOOOe
OOOOOOOOOOOOOOOOOOO@                               aaaaaaa       @@',OOOOn
OOOOOOOOOOOOOOOOOOO@                        aaa@@@@@@@@""        @@ OOOOOi
OOOOOOOOOO~~ aaaaaa"a                 aaa@@@@@@@@@@""            @@ OOOOOx
OOOOOO aaaa@"""""""" ""            @@@@@@@@@@@@""               @@@|`OOOO'
OOOOOOOo`@@a                  aa@@  @@@@@@@""         a@        @@@@ OOOO9
OOOOOOO'  `@@a               @@a@@   @@""           a@@   a     |@@@ OOOO3
`OOOO'       `@    aa@@       aaa"""          @a        a@     a@@@',OOOO'


There's been a murder in Terminal City, and TCPD needs your help.

To figure out whodunit, go to the "mystery" sub-directory and start working from there.

You'll want to start by collecting all the clues at the crime scene (the "crimescene" file).

The officers on the scene are pretty meticulous, so they've written down EVERYTHING in their officer reports.

Fortunately the sergeant went through and marked the real clues with the word "CLUE" in all caps.

If you get stuck, open one of the hint files (from the Command Line, type "cat hint1", "cat hint2", etc.).

For tips on getting started with the Command Line, open "cheatsheet.md".

Don't use a text editor to view any files except "readme.md" and "cheatsheet.md".
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ ls
Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint1
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint2
Sarahs-MacBook-Pro:mystery sarah$ grep "CLUE" crimescene
CLUE: Footage from an ATM security camera is blurry but shows that the perpetrator is a tall male, at least 6'.
CLUE: Found a wallet believed to belong to the killer: no ID, just loose change, and membership cards for AAA, Delta SkyMiles, the local library, and the Museum of Bash History. The cards are totally untraceable and have no name, for some reason.
CLUE: Questioned the barista at the local coffee shop. He said a woman left right before they heard the shots. The name on her latte was Annabel, she had blond spiky hair and a New Zealand accent.
Sarahs-MacBook-Pro:mystery sarah$ 

Sarahs-MacBook-Pro:~ sarah$ cd wdi
Sarahs-MacBook-Pro:wdi sarah$ cd command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ ls
cheatsheet.md	hint2		hint4		hint6		hint8		mystery		solution.md
hint1		hint3		hint5		hint7		instructions	readme.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd cat instructions
-bash: cd: cat: No such file or directory
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat instructions
.OOOOOOOOOOOOOOO @@                                   @@ OOOOOOOOOOOOOOOO.
OOOOOOOOOOOOOOOO @@                                    @@ OOOOOOOOOOOOOOOO
OOOOOOOOOO'''''' @@                                    @@ ```````OOOOOOOOO
OOOOO'' aaa@@@@@@@@@@@@@@@@@@@@"""                   """""""""@@aaaa `OOOO
OOOOO,""""@@@@@@@@@@@@@@""""                                     a@"" OOOA
OOOOOOOOOoooooo,                                            |OOoooooOOOOOS
OOOOOOOOOOOOOOOOo,                                          |OOOOOOOOOOOOC
OOOOOOOOOOOOOOOOOO                                         ,|OOOOOOOOOOOOI
OOOOOOOOOOOOOOOOOO @          THE                          |OOOOOOOOOOOOOI
OOOOOOOOOOOOOOOOO'@           COMMAND                      OOOOOOOOOOOOOOb
OOOOOOOOOOOOOOO'a'            LINE                         |OOOOOOOOOOOOOy
OOOOOOOOOOOOOO''              MURDERS                      aa`OOOOOOOOOOOP
OOOOOOOOOOOOOOb,..                                          `@aa``OOOOOOOh
OOOOOOOOOOOOOOOOOOo                                           `@@@aa OOOOo
OOOOOOOOOOOOOOOOOOO|                                             @@@ OOOOe
OOOOOOOOOOOOOOOOOOO@                               aaaaaaa       @@',OOOOn
OOOOOOOOOOOOOOOOOOO@                        aaa@@@@@@@@""        @@ OOOOOi
OOOOOOOOOO~~ aaaaaa"a                 aaa@@@@@@@@@@""            @@ OOOOOx
OOOOOO aaaa@"""""""" ""            @@@@@@@@@@@@""               @@@|`OOOO'
OOOOOOOo`@@a                  aa@@  @@@@@@@""         a@        @@@@ OOOO9
OOOOOOO'  `@@a               @@a@@   @@""           a@@   a     |@@@ OOOO3
`OOOO'       `@    aa@@       aaa"""          @a        a@     a@@@',OOOO'


There's been a murder in Terminal City, and TCPD needs your help.

To figure out whodunit, go to the "mystery" sub-directory and start working from there.

You'll want to start by collecting all the clues at the crime scene (the "crimescene" file).

The officers on the scene are pretty meticulous, so they've written down EVERYTHING in their officer reports.

Fortunately the sergeant went through and marked the real clues with the word "CLUE" in all caps.

If you get stuck, open one of the hint files (from the Command Line, type "cat hint1", "cat hint2", etc.).

For tips on getting started with the Command Line, open "cheatsheet.md".

Don't use a text editor to view any files except "readme.md" and "cheatsheet.md".
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ ls
Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint1
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint2
Sarahs-MacBook-Pro:mystery sarah$ grep "CLUE" crimescene
CLUE: Footage from an ATM security camera is blurry but shows that the perpetrator is a tall male, at least 6'.
CLUE: Found a wallet believed to belong to the killer: no ID, just loose change, and membership cards for AAA, Delta SkyMiles, the local library, and the Museum of Bash History. The cards are totally untraceable and have no name, for some reason.
CLUE: Questioned the barista at the local coffee shop. He said a woman left right before they heard the shots. The name on her latte was Annabel, she had blond spiky hair and a New Zealand accent.
Sarahs-MacBook-Pro:command-line-mystery sarah$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   solution.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	mystery/solution.md
	notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
Sarahs-MacBook-Pro:command-line-mystery sarah$ git add .
Sarahs-MacBook-Pro:command-line-mystery sarah$ git commit -m "saving commands"
[master 78374d9] saving commands
 3 files changed, 116 insertions(+)
 create mode 100644 mystery/solution.md
 create mode 100644 notes.txt
Sarahs-MacBook-Pro:command-line-mystery sarah$

Sarahs-MacBook-Pro:~ sarah$ cd wdi
Sarahs-MacBook-Pro:wdi sarah$ cd command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ ls
cheatsheet.md	hint2		hint4		hint6		hint8		mystery		solution.md
hint1		hint3		hint5		hint7		instructions	readme.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd cat instructions
-bash: cd: cat: No such file or directory
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat instructions
.OOOOOOOOOOOOOOO @@                                   @@ OOOOOOOOOOOOOOOO.
OOOOOOOOOOOOOOOO @@                                    @@ OOOOOOOOOOOOOOOO
OOOOOOOOOO'''''' @@                                    @@ ```````OOOOOOOOO
OOOOO'' aaa@@@@@@@@@@@@@@@@@@@@"""                   """""""""@@aaaa `OOOO
OOOOO,""""@@@@@@@@@@@@@@""""                                     a@"" OOOA
OOOOOOOOOoooooo,                                            |OOoooooOOOOOS
OOOOOOOOOOOOOOOOo,                                          |OOOOOOOOOOOOC
OOOOOOOOOOOOOOOOOO                                         ,|OOOOOOOOOOOOI
OOOOOOOOOOOOOOOOOO @          THE                          |OOOOOOOOOOOOOI
OOOOOOOOOOOOOOOOO'@           COMMAND                      OOOOOOOOOOOOOOb
OOOOOOOOOOOOOOO'a'            LINE                         |OOOOOOOOOOOOOy
OOOOOOOOOOOOOO''              MURDERS                      aa`OOOOOOOOOOOP
OOOOOOOOOOOOOOb,..                                          `@aa``OOOOOOOh
OOOOOOOOOOOOOOOOOOo                                           `@@@aa OOOOo
OOOOOOOOOOOOOOOOOOO|                                             @@@ OOOOe
OOOOOOOOOOOOOOOOOOO@                               aaaaaaa       @@',OOOOn
OOOOOOOOOOOOOOOOOOO@                        aaa@@@@@@@@""        @@ OOOOOi
OOOOOOOOOO~~ aaaaaa"a                 aaa@@@@@@@@@@""            @@ OOOOOx
OOOOOO aaaa@"""""""" ""            @@@@@@@@@@@@""               @@@|`OOOO'
OOOOOOOo`@@a                  aa@@  @@@@@@@""         a@        @@@@ OOOO9
OOOOOOO'  `@@a               @@a@@   @@""           a@@   a     |@@@ OOOO3
`OOOO'       `@    aa@@       aaa"""          @a        a@     a@@@',OOOO'


There's been a murder in Terminal City, and TCPD needs your help.

To figure out whodunit, go to the "mystery" sub-directory and start working from there.

You'll want to start by collecting all the clues at the crime scene (the "crimescene" file).

The officers on the scene are pretty meticulous, so they've written down EVERYTHING in their officer reports.

Fortunately the sergeant went through and marked the real clues with the word "CLUE" in all caps.

If you get stuck, open one of the hint files (from the Command Line, type "cat hint1", "cat hint2", etc.).

For tips on getting started with the Command Line, open "cheatsheet.md".

Don't use a text editor to view any files except "readme.md" and "cheatsheet.md".
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ ls
Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint1
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint2
Sarahs-MacBook-Pro:mystery sarah$ grep "CLUE" crimescene
CLUE: Footage from an ATM security camera is blurry but shows that the perpetrator is a tall male, at least 6'.
CLUE: Found a wallet believed to belong to the killer: no ID, just loose change, and membership cards for AAA, Delta SkyMiles, the local library, and the Museum of Bash History. The cards are totally untraceable and have no name, for some reason.
CLUE: Questioned the barista at the local coffee shop. He said a woman left right before they heard the shots. The name on her latte was Annabel, she had blond spiky hair and a New Zealand accent.
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat notes.txt>>solution.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   solution.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	mystery/solution.md
	notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
Sarahs-MacBook-Pro:command-line-mystery sarah$ git add .
Sarahs-MacBook-Pro:command-line-mystery sarah$ git commit -m "saving commands"
[master 78374d9] saving commands
 3 files changed, 116 insertions(+)
 create mode 100644 mystery/solution.md
 create mode 100644 notes.txt
 Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint3
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ grep "Annabel" people
Annabel Sun	F	26	Hart Place, line 40
Oluwasegun Annabel	M	37	Mattapan Street, line 173
Annabel Church	F	38	Buckingham Place, line 179
Annabel Fuglsang	M	40	Haley Street, line 176

Sarahs-MacBook-Pro:mystery sarah$ head -n 20 people
***************
To go to the street someone lives on, use the file
for that street name in the 'streets' subdirectory.
To knock on their door and investigate, read the line number
they live on from the file.  If a line looks like gibberish, you're at the wrong house.
***************

NAME	GENDER	AGE	ADDRESS
Alicia Fuentes	F	48	Walton Street, line 433
Jo-Ting Losev	F	46	Hemenway Street, line 390
Elena Edmonds	F	58	Elmwood Avenue, line 123
Naydene Cabral	F	46	Winthrop Street, line 454
Dato Rosengren	M	22	Mystic Street, line 477
Fernanda Serrano	F	37	Redlands Road, line 392
Emiliano Wenk	M	90	Paulding Street, line 490
Larry Lapin	M	71	Atwill Road, line 298
Jakub Gondos	M	61	Mitchell Street, line 187
Derek Kazanin	M	55	Tennis Road, line 440
Jens Tuimalealiifano	M	83	Rockwood Street, line 205
Nikola Kadhi	M	75	Glenville Avenue, line 226
Sarahs-MacBook-Pro:mystery sarah$

Sarahs-MacBook-Pro:~ sarah$ cd wdi
Sarahs-MacBook-Pro:wdi sarah$ cd command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ ls
cheatsheet.md	hint2		hint4		hint6		hint8		mystery		solution.md
hint1		hint3		hint5		hint7		instructions	readme.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd cat instructions
-bash: cd: cat: No such file or directory
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat instructions
.OOOOOOOOOOOOOOO @@                                   @@ OOOOOOOOOOOOOOOO.
OOOOOOOOOOOOOOOO @@                                    @@ OOOOOOOOOOOOOOOO
OOOOOOOOOO'''''' @@                                    @@ ```````OOOOOOOOO
OOOOO'' aaa@@@@@@@@@@@@@@@@@@@@"""                   """""""""@@aaaa `OOOO
OOOOO,""""@@@@@@@@@@@@@@""""                                     a@"" OOOA
OOOOOOOOOoooooo,                                            |OOoooooOOOOOS
OOOOOOOOOOOOOOOOo,                                          |OOOOOOOOOOOOC
OOOOOOOOOOOOOOOOOO                                         ,|OOOOOOOOOOOOI
OOOOOOOOOOOOOOOOOO @          THE                          |OOOOOOOOOOOOOI
OOOOOOOOOOOOOOOOO'@           COMMAND                      OOOOOOOOOOOOOOb
OOOOOOOOOOOOOOO'a'            LINE                         |OOOOOOOOOOOOOy
OOOOOOOOOOOOOO''              MURDERS                      aa`OOOOOOOOOOOP
OOOOOOOOOOOOOOb,..                                          `@aa``OOOOOOOh
OOOOOOOOOOOOOOOOOOo                                           `@@@aa OOOOo
OOOOOOOOOOOOOOOOOOO|                                             @@@ OOOOe
OOOOOOOOOOOOOOOOOOO@                               aaaaaaa       @@',OOOOn
OOOOOOOOOOOOOOOOOOO@                        aaa@@@@@@@@""        @@ OOOOOi
OOOOOOOOOO~~ aaaaaa"a                 aaa@@@@@@@@@@""            @@ OOOOOx
OOOOOO aaaa@"""""""" ""            @@@@@@@@@@@@""               @@@|`OOOO'
OOOOOOOo`@@a                  aa@@  @@@@@@@""         a@        @@@@ OOOO9
OOOOOOO'  `@@a               @@a@@   @@""           a@@   a     |@@@ OOOO3
`OOOO'       `@    aa@@       aaa"""          @a        a@     a@@@',OOOO'


There's been a murder in Terminal City, and TCPD needs your help.

To figure out whodunit, go to the "mystery" sub-directory and start working from there.

You'll want to start by collecting all the clues at the crime scene (the "crimescene" file).

The officers on the scene are pretty meticulous, so they've written down EVERYTHING in their officer reports.

Fortunately the sergeant went through and marked the real clues with the word "CLUE" in all caps.

If you get stuck, open one of the hint files (from the Command Line, type "cat hint1", "cat hint2", etc.).

For tips on getting started with the Command Line, open "cheatsheet.md".

Don't use a text editor to view any files except "readme.md" and "cheatsheet.md".
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ ls
Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint1
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint2
Sarahs-MacBook-Pro:mystery sarah$ grep "CLUE" crimescene
CLUE: Footage from an ATM security camera is blurry but shows that the perpetrator is a tall male, at least 6'.
CLUE: Found a wallet believed to belong to the killer: no ID, just loose change, and membership cards for AAA, Delta SkyMiles, the local library, and the Museum of Bash History. The cards are totally untraceable and have no name, for some reason.
CLUE: Questioned the barista at the local coffee shop. He said a woman left right before they heard the shots. The name on her latte was Annabel, she had blond spiky hair and a New Zealand accent.
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat notes.txt>>solution.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   solution.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	mystery/solution.md
	notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
Sarahs-MacBook-Pro:command-line-mystery sarah$ git add .
Sarahs-MacBook-Pro:command-line-mystery sarah$ git commit -m "saving commands"
[master 78374d9] saving commands
 3 files changed, 116 insertions(+)
 create mode 100644 mystery/solution.md
 create mode 100644 notes.txt
 Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint3
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ grep "Annabel" people
Annabel Sun	F	26	Hart Place, line 40
Oluwasegun Annabel	M	37	Mattapan Street, line 173
Annabel Church	F	38	Buckingham Place, line 179
Annabel Fuglsang	M	40	Haley Street, line 176

Sarahs-MacBook-Pro:mystery sarah$ head -n 20 people
***************
To go to the street someone lives on, use the file
for that street name in the 'streets' subdirectory.
To knock on their door and investigate, read the line number
they live on from the file.  If a line looks like gibberish, you're at the wrong house.
***************

NAME	GENDER	AGE	ADDRESS
Alicia Fuentes	F	48	Walton Street, line 433
Jo-Ting Losev	F	46	Hemenway Street, line 390
Elena Edmonds	F	58	Elmwood Avenue, line 123
Naydene Cabral	F	46	Winthrop Street, line 454
Dato Rosengren	M	22	Mystic Street, line 477
Fernanda Serrano	F	37	Redlands Road, line 392
Emiliano Wenk	M	90	Paulding Street, line 490
Larry Lapin	M	71	Atwill Road, line 298
Jakub Gondos	M	61	Mitchell Street, line 187
Derek Kazanin	M	55	Tennis Road, line 440
Jens Tuimalealiifano	M	83	Rockwood Street, line 205
Nikola Kadhi	M	75	Glenville Avenue, line 226
Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat notes.txt>>solution.md
Sarahs-MacBook-Pro:command-line-mystery sarah$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   notes.txt
	modified:   solution.md

no changes added to commit (use "git add" and/or "git commit -a")
Sarahs-MacBook-Pro:command-line-mystery sarah$ git add .
Sarahs-MacBook-Pro:command-line-mystery sarah$ git commit -m "update to solutions"
[master 766e1df] update to solutions
 2 files changed, 243 insertions(+), 1 deletion(-)

 Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
 Sarahs-MacBook-Pro:mystery sarah$ grep "Annabel" people
 Annabel Sun	F	26	Hart Place, line 40
 Oluwasegun Annabel	M	37	Mattapan Street, line 173
 Annabel Church	F	38	Buckingham Place, line 179
 Annabel Fuglsang	M	40	Haley Street, line 176
 Sarahs-MacBook-Pro:mystery sarah$ head -n 173 streets/Mattapan_Street | tail -n 1
 SEE INTERVIEW #9437737
 Sarahs-MacBook-Pro:mystery sarah$ ls
 crimescene	interviews	memberships	people		solution.md	streets		vehicles
 Sarahs-MacBook-Pro:mystery sarah$ head -n40 streets/Hart_Place | tail -n 1
 SEE INTERVIEW #47246024
 Sarahs-MacBook-Pro:mystery sarah$ head -n179 streets/Buckingham_Place | tail -n 1
 SEE INTERVIEW #699607
Sarahs-MacBook-Pro:~ sarah$ cd interviews
Sarahs-MacBook-Pro:interviews sarah$ cat interview-47246024
Ms. Sun has brown hair and is not from New Zealand.  Not the witness from the cafe.
Sarahs-MacBook-Pro:interviews sarah$ cat interview-9437737
Doesn't appear to be the witness from the cafe, who is female.Sarahs-MacBook-Pro:interviews sarah$
Sarahs-MacBook-Pro:interviews sarah$ cat interview-699607
Interviewed Ms. Church at 2:04 pm.  Witness stated that she did not see anyone she could identify as the shooter, that she ran away as soon as the shots were fired.

However, she reports seeing the car that fled the scene.  Describes it as a blue Honda, with a license plate that starts with "L337" and ends with "9"Sarahs-MacBook-Pro:interviews sarah$
Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint4
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint5
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint6
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint7
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint8
Sarahs-MacBook-Pro:command-line-mystery sarah$ cd mystery
Sarahs-MacBook-Pro:mystery sarah$ grep -A 5 "L337" vehicles
License Plate L337P89
Make: Honda
Color: Teal
Owner: Mike Bostock
Height: 6'4"
Weight: 173 lbs
--
License Plate L337369
Make: Honda
Color: Blue
Owner: Heather Billings
Height: 5'2"
Weight: 244 lbs
--
License Plate L337DV9
Make: Honda
Color: Blue
Owner: Joe Germuska
Height: 6'2"
Weight: 164 lbs
--
License Plate L3375A9
Make: Honda
Color: Blue
Owner: Jeremy Bowers
Height: 6'1"
Weight: 204 lbs
--

Sarahs-MacBook-Pro:mystery sarah$ cd ~/wdi/command-line-mystery
Sarahs-MacBook-Pro:command-line-mystery sarah$ cat hint8
Sarahs-MacBook-Pro:mystery sarah$ ls
crimescene	interviews	memberships	people		solution.md	streets		vehicles
Sarahs-MacBook-Pro:mystery sarah$ cd memberships
Sarahs-MacBook-Pro:memberships sarah$ ls
AAA			Costco			Fitness_Galaxy		REI			TCSU_Alumni_Association	United_MileagePlus
AAdvantage		Delta_SkyMiles		Museum_of_Bash_History	Rotary_Club		Terminal_City_Library
Sarahs-MacBook-Pro:memberships sarah$ cat AAA Delta_SkyMiles Museum_of_Bash_History Terminal_City_Library | grep -c "Heather Billings"
2
Sarahs-MacBook-Pro:memberships sarah$ cat AAA Delta_SkyMiles Museum_of_Bash_History Terminal_City_Library | grep -c "Joe Germuska"
2
Sarahs-MacBook-Pro:memberships sarah$ cat AAA Delta_SkyMiles Museum_of_Bash_History Terminal_City_Library | grep -c "Mike Bostock"
4
Sarahs-MacBook-Pro:memberships sarah$ cat AAA Delta_SkyMiles Museum_of_Bash_History Terminal_City_Library | grep -c "Jeremy Bowers"
4

Mike Bostock & Jeremy Bowers both have the same memberships, but Mike's car is described as Teal and Jeremy's is the true Blue Honda.
So the perpetrator must be Jeremy Bowers.
