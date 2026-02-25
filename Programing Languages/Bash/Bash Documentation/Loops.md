
In Bash there are 3 types of loops the `while`, the `for` and the `until` loops

### While

- Used when you **don’t know in advance** how many times the loop should run.
- It continues as long as the condition remains true.

```bash
count=1 
while [ $count -le 5 ]; do 
	echo "Count is $count" 
	((count++)) 
done
```

### Until

- Until loops are similar to while loops, but they execute until a specified condition becomes true.

```bash
count=1 
until [ $count -gt 5 ]; do 
	echo "Count is $count" 
	((count++)) 
done
```
### For

- Used when you **do know** how many times to repeat, or when you're iterating over a sequence (like a list, string, or range).
- It's great for looping through items.

```bash
for i in {1..5}; do 
	echo "Iteration $i" 
done
```
