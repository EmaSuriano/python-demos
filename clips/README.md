## How to use Fuzzy clips?

- Open FZ clips (binary already compiled):

```bash
$ ./fz_clips
```

- Load programs by running:

```bash
➜  source git:(master) ✗ ./fz_clips
        FuzzyCLIPS V6.10d (10/22/2004)
FuzzyCLIPS>
```

- Load `deftemplate`, `defrule` and `deffacts`:

```bash
FuzzyCLIPS> (load "PATH_FILE.clp")
```

- Reset to initial values:

```bash
FuzzyCLIPS> (reset)
```

- Show facts:

```bash
FuzzyCLIPS> (facts)
```

- Run the step one by one or all together:

```bash
FuzzyCLIPS> (run 1)
```

```bash
FuzzyCLIPS> (run)
```

- Plot fuzzy graph for fact:

```bash
FuzzyCLIPS> (plot-fuzzy-value t + 1 8 4)
```

- `+`: means the symbol to use for the graph
- `1 8`: is the range for the plot
- `4`: is the fact to show

- Defuzzify fact

```bash
FuzzyCLIPS> (moment-defuzzify 4)
```

## Add formatting and some basic syntax checking with VScode

Given that LISP shared some similarities with Clojure language in the way they define the paranthesis we can actually make use of many of the formatters out there!

Just installed any formatter extension and then open your `.clp` file. There run `Cmd+Shift+P` and select `Change Language Mode`. In the list look for Clojure and select it.

The icon of the file should have changed. Now open the menu again by running `Cmd+Shift+P` and select `Format Document`, there you should be able to select the new formatter you installed.

In that moment your code should get formatted to the configuration that you set it up to.

Besides formatting you also gain the perk of checking of the syntax is indeed correct, without the need of loading the program into FuzzyClips. Basically if the formatter fails, it means the syntax is wrong...
