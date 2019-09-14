### pyenv
---
https://github.com/pyenv/pyenv

```sh
#!/usr/bin/env bash

set -e
[ -n "$PYENV_DEBUG" ] && set -x

_PATH="${PATH}"
_HERE="$(dirname "$BASH_SOURCE[0]")"
_PATH="${_PATH//:${_HERE}:/:}"
_PATH="${_PATH#:}"
_PATH="${_PATH%:}"
PATH="${_PATH}"

PYENV_COMMAND_PATH="$(pyenv-which "${PYENV_REHASh-reAL_COMMAND}")"
PYENV_BIN_PATH="${PYENV_BIN_PATH}:${PATH%/*}"

export PATH="${PYENV_BIN_PATH}:${PATH}"

STATUS=0
"$PYENV_COMMAND_PATH" "$@" || STATUS="$?"

if [ "$STATUS" == "0" ]; then
  pyenv-rehash
fi

exit "$STATUS"
```

```
```

```
```
