[Back to Main](../README.md)

# Print Shapes

> Pixel art

<details>

<summary>Authors</summary>

Dicaprio Cheung (dhcheungaa@connect.ust.hk)

</details>

It is recommended to understand everything before `Control Flow` before attempting this homework

## Level 1 : Warm Up

In this assignment, we would like to draw some shapes with the character "*"

First, we will ask the user to tell us the size of the shape with the prompt `"size? "`
Then, the program should draw the shape given in the image:

![](../../images/basic-shape.png)

#### Example
```
size? 3
*
**
***
```

```
size? 5
*
**
***
****
*****
```

## Level 2 : Actual Homework

Totally same with Level 1 but draw a much bigger shape (only draw the red part)

![](../../images/shape.png)

#### Example

![](../images/print-shapes-example.png)

The parallelogram has length 3 given `n=2`

**Please note that this screenshot of the text is the correct output for `n=2`, we meant the side length of the left triangle is n in the previous picture**

**Please note that spaces are indicated by the hollow rectangles ▯. Otherwise, there are nothing. This means that the empty line on the fourth row is done via newline `\n`**

You can assume the size is an integer > 1


int N = 2 * size + 1;
	int H = 3 * size + 2;

	for (int y = 0; y < H; y++)
	{
		// the first part
		if (y < size)
		{
			for (int x = 0; x < N; x++)
			{
				if (x < size - y)
					printf("*");
				else if (x < size + 1 + y)
					printf(" ");
				else
					printf("*");
			}

			printf("\n");
		}
		else if (y == size)
		{
			printf("\n");
		}
		// the second part
		else if (y > size && y < N)
		{
			int dy = y - size;
			for (int x = 0; x < N; x++)
			{
				if (x < dy)
					printf("*");
				else if (x < N - dy)
					printf(" ");
				else
					printf("*");
			}

			printf("\n");
		}
		else if (y == N)
		{
			printf("\n");
		}
		// the third part
		else if (y > N)
		{
			int dy = y - N;
			for (int x = 0; x < N + size; x++)
			{
				if (x < size)
					printf("*");
				else if (x < size + dy)
					printf(" ");
				else if (x > N + dy - 2)
					printf(" ");
				else
					printf("*");
			}

			printf("\n");
		}
	}
}



int main(int argc, char *argv[])
{
	while (1)
	{
		int size = 0;
		printf("\nPlease enter the shape size: ");
		scanf("%d", &size);
		printf("\n");

		if (size == 0)
			break;

		//draw_level_1_shape(size);
		draw_level_2_shape(size);
	}
	
	return 0;
}


## How to Run Your Code

To run the code, you need to make sure that you are first in the right folder/directory in your terminal (the text area under your code):
Currently, in the example, the user is in the directory `/workspaces/codespaces-blank` you need to get to `/workspaces/codespaces-blank/<homework-repository-name>/hw3` to run your `main.c` code, do this by writing the command `cd <homework-repository-name>/hw3` (cd: change directory) and press enter.

(Note: if you want to go up a folder you can use `cd ..`)

![image](./../images/462ba8f7-a31a-4797-86fc-250e2d353d8e.png)

Note that you need to do this everytime you open the Github Codespace.

Once you are in the direcctory, run the following command in the terminal:
```
gcc -o homework.exe main.c && ./homework.exe
```
(Note: for a C code to run, we need to make it an executable file, then run it)

![image](./../images/368292205-462ba8f7-a31a-4797-86fc-250e2d353d8e.png)



## Submission

Modify `main.c` in the `hw3` folder containing your *level 2* code for your homework. We will not grade your level 1 code. Refer to the [Main README.md](../README.md) for details.

