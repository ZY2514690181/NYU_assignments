yz5892trainHMM_HW3 is the Jupyter notebook for the main program.

Each section has comment that indicates what it does.

To run the code, run all the sections following the order. For easy-to-grade purpose, the program assumes that the training file is named as "WSJ_24.pos" and "WSJ_02-21.pos" already so no inputs are needed. One way to slightly improve the program is to add lines that ask for user inputs.

The beginning of the program is basic setup and training, where the program takes training and development files and build transition tables and likelihood tables. In the process, the states and words are collected in lists. Words that appear only once are used to simulate OOV words distribution.

Then the test file is imported and analyzed by sentences. Viterbi table and backpointer table are used. Each word in the sentence is then assigned a tag that is most likely to be correct. When there is an OOV word, apply the OOV words distribution learned before.

When the program finishes and all the outcomes are written to "submission.pos", there is an out of index error for list, so use try-except to avoid it. The program takes hours to run in total and generates neat output.