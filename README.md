## Sprint Coding Challenge 1

Write a function that allocates an array of `int`s of a specified size.
(The `cols` parameter holds the size.)

```c
int *alloc_1d(int cols)
{
	// !!! IMPLEMENT ME
	// (solution is about 2 lines of code)
}

void alloc_1d_example(void)
{
	int *my_array = alloc_1d(12);

	my_array[8] = 3490;

	// The same array access could be made with pointer arithmetic:
	*(my_array+8) = 3490;

	// By the C spec, the array notation and pointer arithmetic notation
	// are 100% equivalent.

	printf("my_array[8] = %d\n", my_array[8]);
}

```

## Sprint Coding Challenge 2

Write a function that allocates a two-dimensional array of `int`s of a
specified size. (The `rows` parameter is how many rows in the array, and
`cols` is how many columns per row.)

```c
int **alloc_2d(int rows, int cols)
{
	// !!! IMPLEMENT ME
	// (solution is about 5 lines of code)
}

void alloc_2d_example(void)
{
	int **my_array = alloc_2d(5, 10);

	// First array index is row, second is column:
	my_array[2][3] = 3490;

	// The same array access could be made with pointer arithmetic:
	*(*(my_array+2)+3) = 3490;

	// By the C spec, the array notation and pointer arithmetic notation
	// are 100% equivalent.
	
	printf("my_array[2][3] = %d\n", my_array[2][3]);
}
```
