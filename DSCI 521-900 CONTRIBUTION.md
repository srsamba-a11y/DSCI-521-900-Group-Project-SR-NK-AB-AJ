attribute_counts = FARS_2022.groupby('STATENAME').size() #grouping by attribute STATENAME
attributes_sorted = attribute_counts.sort_values(ascending=False) #sorting by most to least

attribute_counts2 = FARS_2023.groupby('STATENAME').size()
attributes_sorted2 = attribute_counts2.sort_values(ascending=False)
