::

    Syntax: turnkey-lxc-info [-h] [-p|-u|-n]

    Probes system for LXC priviledge level.

    Options:
        -h|--help       - Show this help and exit
        -p|--is-priv    - exit 0 if privileged; otherwise 1
        -u|--is-unpriv  - exit 0 if unprivileged (inc nested); otherwise 1
        -n|--is-nested  - exit 0 if nested; otherwise 1

    With no switch (and no error), it will exit 0 and output one of the
    following:

        privileged      - if container is privileged
        unprivileged    - if container is unprivileged
        nested          - if container is nested (implies unprivileged too)

    If a switch other than -h|--help is used, then there will be no text output
    on stdout (stderr if any errors), exit code will be as noted above.

    If not run within an LXC container, it will exit 1 with error message on
    stderr. Running as root is recommended (but not strictly required).
