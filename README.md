# HS Static Analysis
We've decided to use ![Python 3](https://img.shields.io/badge/python-3-blue.svg).

Open PRs!

## Code style
Please use [PEP 8](https://www.python.org/dev/peps/pep-0008/) (for styling) and [PEP 484](https://www.python.org/dev/peps/pep-0484/) (for type hinting in all functions).

## What to do
We need the following parts:

### Interface: Stepik step checker
This is a class that receives HTML text (like a Stepik text) and returns a verdict: is the text right or not.

Think about the signature of the function.

### Implementations
Then create some classes implementing the interface. You can use libraries like the  `beautiful soup` to parse the text.

Don't forget that some checks are irrelevant for text in the `<code>` tag.

The list of checkers:

TODO. First of all, choose and create a single one (better from the start). After completing all the parts, implement others:
1. **Usage of `args: Array<String>`** in Kotlin coding tasks templates.
1. **Hyphen** (-) instead of a *dash* (–) [how to check: search for space-hyphen-space].
1. **Double hyphen** instead of a *dash*.
1. Test count in a coding task **is small** [let's say `MINIMUM_TEST_COUNT = 5`].
1. **Repeating spaces**.
1. **Lesson/lessons** instead of *topic/topics*.
1. **Unusual quotes** (‘’ or “” – like commas) instead of *normal ones* (' or ") [<--- this happens when you copy-paste your text from Google Docs to Stepik].
1. Gender neutrality (**she he** instead of they, don't forget about **her his**).
1. **Usage of `Scanner`** class in Kotlin coding tasks templates.
1. **Cyrillic letters**.
1. Wrong answer hints **aren't set** [we are going to add hints like "which paragraph contains the needed info"].
1. **Multiple HINTs** in the task.

Done:

When you add a checker, move it here.

### Tests
Provide tests for every implementation. Inspiration can be found [here](https://github.com/SerVB/compression-server/blob/b66cdea12232ebeac58010b30235289cb1bfd1e8/tests.py) (the `unittest` library).

### CI
I will set up GitHub Actions once there is a test.

### Mechanism to suppress warnings
We need a way to suppress wrong warnings. I guess it will be a file with lines of text which should be removed before checking. The file will be unique for each checker and for each step.

Add tests.

### HS crawler
We need some code that goes through HS topics and calls all the implementations on them.

You can use the following ways to collect the texts:
1. [HS API](https://hyperskill.org/api/steps?format=api) ([docs](https://hyperskill.org/api/docs/)).
1. Stepik API.