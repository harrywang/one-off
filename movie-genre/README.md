The key challenge is converting the following "list-like" string into a real list:

```
"[{'id': 16, 'name': 'Animation'}, {'id': 35, 'name': 'Comedy'}, {'id': 10751, 'name': 'Family'}]"
```

`ast.literal_eval` does the trick: https://docs.python.org/2/library/ast.html

Another useful part is converting a list of list into a csv file using pandas:

```
my_df = pd.DataFrame(my_list)
my_df.to_csv('my_csv.csv', index=False, header=False)
```
