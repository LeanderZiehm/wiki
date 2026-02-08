
# Venv


# uv

## install 
curl -LsSf https://astral.sh/uv/install.sh | sh

## use
uv manages project dependencies and environments, with support for lockfiles, workspaces, and more, similar to rye or poetry:
uv init example
cd example
uv add ruff
uv run ruff check
uv lock
uv sync


# ruff

# Create a virtual environment
python -m venv myenv

# Activate on Windows
myenv\Scripts\activate

# Activate on macOS/Linux
source myenv/bin/activate

# Deactivate
deactivate
