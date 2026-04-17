# **Information-Geometric Hyperscanning for Inter-Brain Networks**

<p align="center">
<img src="brainhack_figure.png" alt="Information-Geometric Hyperscanning Network Circular Graph" width="250">
</p>

## **BrainHack Warsaw 2026**  
Welcome to the HyPhi(Φ) project repository for BrainHack Warsaw!  

HyPhi(Φ) is a scalable hyperscanning analysis pipeline that characterizes inter-brain coupling using discrete Ricci curvature and curvature entropy. Instead of treating inter-brain synchrony as a scalar quantity, we model time-resolved inter-brain networks as evolving geometric objects.

**Project coordinators**

Nicolás Hinrichs

Nahid Torbati

**Contributors**

Kacper Łyczak

Vinayak M. Kulkarni

Katarzyna Libera

Pola Kukiełka

Hanna Święcicka

Marta Lotka

Sylwia Adamus

Zuzanna Maruszewska

## **🗺️ Conceptual Map & Pipeline**

Our analysis workflow bridges established hyperscanning ecosystems with novel geometric measures. The pipeline follows these core steps:

1. [**HyPyP**](https://github.com/GHFC/HyPyP) Preprocess data and extract **adjacency matrices**.  
2. [**NetworkX**](https://networkx.org/) Construct **weighted connectivity** graphs from the matrices.  
3. [**HyPhi**](https://github.com/nicolashinrichs/HyPhi) Conduct **curvature analyses** on the resulting networks.

Mattermost handle:
[https://minervamessenger.mpdl.mpg.de/neural-ds-lab/channels/hyphi](https://minervamessenger.mpdl.mpg.de/neural-ds-lab/channels/hyphi)

## **🗓️ BrainHack Warsaw Schedule**

### **Day 1 (19:30 \- 22:00)**

**Focus:** Project kickoff and data preparation.

* **Who:** All participants  
* **Tasks:**  
  * How to organize and structure our work.  
  * Grant collaborator access to the main HyPhi repository.
  * Create dedicated branches for each team/feature.

### **Day 2**

**Focus:** Core analysis, geometric metrics, and statistical modeling.

* **Who:** Everyone
  * Preprocess the dataset using the HyPyP pipeline.
  * Create initial connectivity matrices using NetworkX.
 
* **Teams & Tasks:**  
  * **Team Red:** Focus on *Spectral Graph Analyses*.  
  * **Team Blue:** Focus on *Entropy* and/or *Wasserstein distance* (heat diffusion probabilities vs. random walking) and/or *Statistical Analyses*.  
  * **Team leaders:** Project coordination/guidance, core pipeline integration, and Flow module.

### **Day 3 (09:00 \- 13:00)**

**Focus:** Wrap-up, documentation, and interpretation.

* **Who:** Everyone  
* **Tasks:**  
  * Repository setup, code commenting, and finalizing README files.  
  * Adding interpretations and conceptual explanations to the findings.

## **🚀 Possible Contributions & Future Directions**

We welcome contributions from coders and non-coders alike\! Potential areas for contribution during the Hackathon and beyond include:

* **Spectral Graph Analyses:** Deeper dives into the spectral properties of inter-brain networks.  
* **Advanced Metrics:** Implementing Wasserstein distance from heat diffusion probabilities vs. random walking.  
* **Tooling:** Developing a Graphic User Interface (GUI) with straightforward options for modality, task, and measure selection.  
* **Conceptualization:** Modeling and interpreting existing synchrony metrics against our geometric ones.

## **🤝 Collaboration & Outputs**

* Code commenting, finalizing README files, and submitting Pull Requests from our dedicated branches.
* Drafting a structural outline for our joint publication to organize our asynchronous work after the event.
* Adding interpretations and conceptual explanations to the findings.
* **Other project participants?** We are actively looking for cognitive neuroscientists, physicists/applied mathematicians, and science visualization specialists to join the effort.


## **📚 Literature**

1. https://www.frontiersin.org/journals/aging-neuroscience/articles/10.3389/fnagi.2023.1120846/full
2. https://www.nature.com/articles/s41598-018-27001-3
3. https://www.nature.com/articles/s41598-020-67474-9
4. https://www.nature.com/articles/s41598-019-46380-9
5. https://www.sciencedirect.com/science/article/abs/pii/S0378437122005179
6. https://math.oit.edu/~hammondd/publications/hammond_gur_johnson_ieee_globalsip_2013.pdf



# How to get started to collaborate

## Setting up the repository

Clone to a desired location on your device

```shell
git clone https://github.com/nicolashinrichs/HyPhi
cd HyPhi
```

Create a branch to develop

```shell
git checkout -b my-feature-branch
```

## Setting up the Python environment

Using the [`uv`](https://docs.astral.sh/uv/) package manager
(if not installed yet, see: https://docs.astral.sh/uv/getting-started/installation/)

Use either the `make` command

```shell
make install
```

Or use uv directly: `uv sync --extra develop --extra notebook`  (leave the `--extra notebook` flag, if not required).

## Adding modules to the `hyphi` package

The `hyphi` package code resides in `./code/hyphi/`.

To add new functionality, there are three ways:

### 1. Add a function to an existing module

For instance, add a function to the existing `./code/hyphi/stats.py`

```python
# ./code/hyphi/stats.py
def my_new_function():
    # do something great
    ...
```

This can be used in another script or notebook in the following way:

```python
from hyphi.stats import my_new_function

# Use the new function
my_new_function()
```

### 2. Add a new submodule with its own functionality in an existing module

Create a new Python file, becoming a submodule of `hyphi` with several functions and or classes.
Place the file where it makes sense:

```shell
touch code/hyphi/visualization/my_viz_tools.py
```

Here, we add a submodule to the `visualization` module of `hyphi`.


Provide functionality in this new submodule:

```python
# code/hyphi/visualization/my_viz_tools.py

def my_viz_function1():
    # great visualization 1
    ...

def my_viz_function2():
    # great visualization 2
    ...
```

Again, this new submodule can be now used in other scripts or notebooks in the following way:

```python
from hyphi.visualization.my_viz_tools import my_viz_function1, my_viz_function2

# Use the new functions
my_viz_function1()
my_viz_function2()
```

### 3. Create a separate module

First, create the container for the new module, that is just a folder:

```shell
mkdir code/hyphi/my_module
```

Then drop an `__init__.py` file in that folder such that Python recognizes the folder as module.

```shell
touch code/hyphi/my_module/__init__.py
```

Then, similar to Option 2 (see [above](#2-add-a-new-submodule-with-its-own-functionality-in-an-existing-module)), create a submodule with its functionality.

```shell
touch code/hyphi/my_module/my_sub_module.py
```

And add functions to it:

```python
# code/hyphi/my_module/my_sub_module.py

def foo():
    # great foo function
    ...

def bar():
    # great bar function
    ...
```

To expose the module directly via `import hyphi` (so that `hyphi.my_module` works without an explicit import), add one line to the main `__init__.py`
at the root of the package folder `./code/hyphi/__init__.py`.

*Note: explicit imports like `from hyphi.my_module.my_sub_module import foo` will work regardless of this step.*

```python
# ./code/hyphi/__init__.py
...

# add this line
import hyphi.my_module  # matches the folder containing the module

...
```

Again, this new module and its submodules can be now used in other scripts or notebooks in the following way:

> **Note:** When adding new functionality, make sure to also add tests (see [below](#add-tests-for-added-functionality)).

```python
from hyphi.my_module.my_sub_module import foo, bar

# Use the new functions
foo()
bar()
```

## Using notebooks

The repository includes template notebooks for interactive exploration and analysis in `./code/notebooks/`:

| Notebook | Format |
|---|---|
| `code/notebooks/hyphi.ipynb` | Jupyter notebook |
| `code/notebooks/hyphi_explore.py` | [marimo](https://marimo.io/) notebook |

### Running notebooks

**Jupyter:**

```shell
uv run --extra notebook jupyter lab code/notebooks/hyphi.ipynb
```

**marimo:**

```shell
uv run --extra notebook marimo edit code/notebooks/hyphi_explore.py
```

> **Note:** Make sure the notebook kernel points to the project's virtual environment (`.venv`) so that `import hyphi` works.

### Creating your own notebooks

If you want to create a new notebook, place it in `./code/notebooks/` to keep things organised:

```shell
# Jupyter
touch code/notebooks/my_analysis.ipynb

# marimo
marimo edit code/notebooks/my_analysis.py
```

Notebooks can also live anywhere else in (or outside) the repository — as long as the `hyphi` package is installed in the active environment, imports will work regardless of the notebook's location.

### Recommended notebook structure

The existing template notebooks follow a common pattern that is worth replicating:

1. **Imports** — load `hyphi` modules and dependencies
2. **Setup** — define global variables and paths
3. **Analysis** — your exploration, visualisation, and computation
4. **Summary** — intermediate or final notes on findings

Starting from a copy of one of the templates is the quickest way to get going:

```shell
cp code/notebooks/hyphi.ipynb code/notebooks/my_analysis.ipynb
```

## Add tests for added functionality

Tests live in `./code/tests/` and use [pytest](https://docs.pytest.org/) conventions.

### 1. Create a test file

For each new (sub)module, create a corresponding test file prefixed with `test_`:

```shell
touch code/tests/test_my_sub_module.py
```

### 2. Write test functions

Test functions must also be prefixed with `test_`. Import the functionality you want to test and assert expected behaviour:

```python
# code/tests/test_my_sub_module.py

from hyphi.my_module.my_sub_module import foo, bar


def test_foo():
    result = foo()
    assert result is not None


def test_bar():
    result = bar()
    assert result == expected_value
```

For related tests, you can group them in a class:

```python
# code/tests/test_my_sub_module.py

class TestFoo:
    """Tests for the foo function."""

    def test_foo_returns_value(self):
        assert foo() is not None

    def test_foo_edge_case(self):
        assert foo(edge_input) == expected_output
```

### 3. Run the tests

Use the `make` command:

```shell
make test
```

Or run pytest directly:

```shell
uv run --extra develop pytest code/tests --cov-report=html -v
```

To run only a specific test file:

```shell
uv run pytest code/tests/test_my_sub_module.py -v
```

