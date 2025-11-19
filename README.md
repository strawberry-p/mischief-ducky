# mischief-ducky

This is a ducky-like python script using the `keyboard` library. It currently targets Windows and relies on `powershell.exe` and `python` being available on the system.

## Effects

The script enters a specified subdir of the Pictures directory, and runs the python REPL in there.
To fulfill the challenge of being offline, I stored a small version of my Work Of Art as hexadecimal characters in the script.

Since even that is a few KB in size, the user has to be a bit cooperative and wait for the mischief script to finish typing (it's probably more annoying to interrupt it, since it will proceed to type out the file wherever your window focus is until you kill it :P). The ducky then converts it to bytes and replaces all .png files in the current folder with it.

The script then exits the repl, moves up to the homedir and down into the testing folder with the same name to replace all .txt files in it with a silly vandalism text (in a "real-world use", this DISARM test directory would be set to "", so the script would replace all images in ~/Pictures and replace all .txt files in ~)

## Running

- Create a `test` directory in your homedir
- Create a `test.txt` file in it
- Similarly, create a `test` directory in ~/Pictures, and a new (empty or not) `test.png` file in it
- (please do not have a localised name for this directory 💔)
- Download `main.py`
- If not already installed, run `pip install keyboard`
- Run `main.py`

## Video demo
(sorry for low quality, this was recorded from my phone at night)


https://github.com/user-attachments/assets/b4159b29-a2e6-4582-bc18-0c313746a155


