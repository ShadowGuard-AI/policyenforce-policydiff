# policyenforce-PolicyDiff
A command-line tool that compares two security policies (e.g., represented as JSON or YAML files) and highlights the differences, particularly focusing on permissions, allowed actions, and resource constraints.  Uses `jsondiffpatch` for efficient comparison. - Focused on Provides tools to programmatically enforce security policies across systems, such as verifying configuration files against a predefined schema and reporting deviations.

## Install
`git clone https://github.com/ShadowStrikeHQ/policyenforce-policydiff`

## Usage
`python3 main.py policy_file1 policy_file2 [--format json|yaml] [--schema SCHEMA]`

Example: `python3 main.py policy_a.yaml policy_b.yaml --format yaml`

A policy file that is empty, or that does not load as a mapping of policy keys, is rejected with an error and exit code 1. It is never compared as if it were a policy.

## Parameters
- `policy_file1`: Path to the first security policy file (JSON or YAML). Required positional argument.
- `policy_file2`: Path to the second security policy file (JSON or YAML). Required positional argument.
- `-h`: Show help message and exit
- `--format`: Output format, json or yaml. Defaults to json.
- `--schema`: Path to the JSON schema file for validating policies.

## License
Copyright (c) ShadowStrikeHQ
