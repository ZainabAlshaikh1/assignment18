# Homework Assignment 18

[![Assignment 18](https://github.com/PGE323M/assignment18/actions/workflows/main.yml/badge.svg)](https://github.com/PGE323M/assignment18/actions/workflows/main.yml)

## Instructions

Reproduce the [Project 2](https://github.com/PGE323M/project2) reservoir simulation
in CMG by working through the [Project 2 CMG tutorial](https://youtu.be/0wFy36pjdX8).
Use the well locations specified in Project 2: they differ slightly from those in
the video. Keep the reservoir properties, grid, wells, controls, and simulation
times consistent with that project.

Open your simulation in CMG Results 3D and export **Pressure**, in **psi**, at the
**end of day 200**. Follow the property-export steps in the
[2D tutorial](https://youtu.be/4UGY74SJZ-o), selecting the complete reservoir grid.
In current versions of Results, **Export Properties** is labeled at the top of the
main menu. Save the exported text as **`assignment18.txt`** in this repository.
Do not replace the CMG export with manually entered pressures.

## Testing

From the repository directory, run:

```bash
python test.py
```

The checker compares sampled pressures from the exported grid with the supplied
`test.npy` values using a 1 psi absolute tolerance (NumPy's default relative
tolerance is unchanged). If it fails, check your model inputs, well locations,
selected output time, pressure units, and export settings. Python 3.11 and NumPy
are sufficient; CMG itself runs separately from this Python environment.

## Submission

Submit only the CMG-exported **`assignment18.txt`**. Keep your CMG input deck and
other simulation files locally. Do not modify the supplied checker, reference
array, or workflows.

```bash
git add assignment18.txt
git commit -m "Submit Assignment 18"
git push origin master
```

Check your repository's Actions page to confirm the output check passes for the
submitted commit.
