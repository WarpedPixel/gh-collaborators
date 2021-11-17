# GitHub CLI Extension *collaborators*

This is currently only implemented for GitHub organizations.

## Installation
To install use gh itself:
```sh
> gh extension install warpedpixel/gh-collaborators
```
## Usage
Usage is simple:

```sh
> gh collaborators SomeOrganizationIBelongTo
```

Assuming that you have access to that organization named `SomeOrganizationIBelongTo`, the extension will think for a bit and output JSON
that looks like the below. Colalborators will be listed once if they have access to *any* of the repos
under the organization, so for large organizations this may take some time.

```json
[
{ "org" : "SomeOrganizationIBelongTo", "collaborators": [
"CoolProgrammer", "OctoCat"
]}
]
```
Output is in JSON so it can be more easily parsed and queried by something like `jq`.
