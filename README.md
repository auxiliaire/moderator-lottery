# moderator-lottery
Rotate moderators with Github Workflow

## Motive

Keep track of the upcoming moderator in a list of possible candidates by automatically updating the choice in certain intervals.

## Requirements

* The solution should be self hosted
* The solution should be free of charge
* The output should be available for everyone at any time
* A manual re-run should simply get the next candidate
* A manual override should be possible
* Adding new candidates should be possible without code change
* The solution should be calendar independent

## Preconditions

- An issue with ID `1` to host the report
- Github token with appropriate access rights
- An environment called `Workflow` for the repository with the following values set:
    - A secret called WORKFLOW_GH_TOKEN pointing to the personal access token
    - A variable called MODERATOR_INDEX pointing to the current moderator in the list
    - A variable called MODERATOR_LIST containing the names of the candidates in BASH array format (eg.: `('Harry' 'James' 'Heather')`)