# Global Progress Bar

*Alex Hagen*

Progress bars within `Jupyter` or in the terminal are really nice, but once you get past about 5 minutes, you don't
want to keep that window open.  Global Progress Bar (**GPB**) is (currently) a Mac only utility that will render a progress bar in your menu bar.  It's designed for use with `Jupyter`, `cmake`, and I'll add more.

In `Jupyter` you can add it with a magic, or in `Jupyter`/`python` with the replacement iterator like

```python
%%gpb
for i in range(10):
  sleep(1)
```

or

```python
for i in gpb(range(10)):
  sleep(1)
```

For `cmake`, you can just pipe your output to it

```bash
cmake <all your build options> 1> gpb
```
