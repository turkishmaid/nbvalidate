# nbvalidate
> (editing this in for the n-th time:) Validate nbdev vs. requirements.


Sidenote: after adding functions to `00_core.ipynb` and `notebook2script()` being executed there, the bove  `import` failed like so: `ModuleNotFoundError: No module named 'nbvalidate'`. You have to adapt `lib_name` in `settings.ini` before. Every tiny litte bit like that adds to your reputation, fast.ai :(

This file will become your README and also the index of your documentation.

## Install

`pip install nbvalidate`

## How to use

All persistency will be in a fixed name folder `~/.nbvalidate` below the user's home directory. Without this folder, the module will not work at all. Before using the package, ensure that this folder is in place:

```python
ensure_dotfolder()
```




    True



Sidenote: raises `NameError: name 'Path' is not defined` in `nbvalidate/core.py in dotfolder()`, while `00_core.ipynb` tests fine. Wtf is this again? 

Only deleting the generated `nbvalidate` folder and doing `notebook2script()`
did the trick
Can anything please just _work_ in `nbdev`? I mean, I am willing to accept all sorts of architectural drawbacks like 
- no autocomplete and other IDE basics
- no debugger
- constant notebook/shell switch
- bad templating

to get
- automatic packaging
- GitHub pages generation (oversold als "literate programming")
- cool CI template

But these permanent mini-fails will likely kick `nbdev` out again. But maybe it's just distracting from the fact that the architectural issues are by far outweigthing the advantages.
