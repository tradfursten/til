# Filtering elements in a list that does not match

If you have one list of thing (passages in the example) and want to find all participants that has not passed a passage.
First you can create a list of only the id:s of the participants that has passed.
Then you can filter the list of all participants using the [member/2](https://hexdocs.pm/elixir/Enum.html#member?/2) function and inversing the result.
```
passages_ids = passages
|> Enum.map(&(&1.participant_id))

missing_participants = participants
|> Enum.filter(&(Enum.member?(passages_id, &1.id) == false)
```