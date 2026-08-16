mkdir python-drills && cd python-drills
git init
python -m venv .venv                  # creates the sealed environment in .venv/
source .venv/Scripts/activate         # Windows Git Bash path (not bin/). Prompt gains (.venv)
python -c "import sys; print(sys.prefix)"   # → inside .venv  ← the health rule, new twist:
                                      # a venv WANTS prefix pointing at itself. The file that
                                      # makes this work is .venv/pyvenv.cfg — the same mechanism
                                      # that, misplaced, wrecked your old interpreter.
pip install ruff