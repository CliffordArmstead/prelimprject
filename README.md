# Howard ID
ID = "@03006886"
# Calculate N = ID % 7
N = int(ID[1:]) % 7

# Calculate X = ID % 9 + 10
X = int(ID[1:]) % 9 + 10

# Iterate to print the strings
for i in range(X):
    start_index = (i + N) % 9
    if start_index == 0:
        print(ID)
    else:
        print(ID[start_index:] + ID[:start_index], end='')
    if i != X - 1:
        print()  # Newline for all strings except the last one
