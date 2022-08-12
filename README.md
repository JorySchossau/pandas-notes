# pandas-notes
I'm tired of forgetting these commands, and there are too many variations online to discover these again.

```py
# read
csv.rename(columns={'sequence':'seq', 'fitness':'prop'}, inplace=True)
# merge
newdf = csv.merge(extradf, on='sequence', how='left')
# rename
csv.rename(columns={'sequence':'seq', 'fitness':'prop'}, inplace=True)
# subset
csv.query('sequence.str.len() > 12')
# alter
csv.loc[csv.query(f'seq.str.len() == {n}').index, 'seq'] += '_suffix'
# drop
csv.drop(some_subset.index, inplace=True)

# create empty-like (similar to python-style list copying)
emptydf = csv.iloc[0:0]
# adding rows
allrowsdf = pd.concat([df1, df2])
# adding cols
allcolsdf = pd.concat([df1, df2], axis=1)
```
