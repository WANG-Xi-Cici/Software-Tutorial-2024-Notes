[Back to Main](../README.md)

# Swapping Contents

> A is B, B is A

Implement your code such that the values of a and b are swapped

```c
#include <stdio.h>

int main() {
    float float1 = 4.0f, float2 = 3.7f;
    printf("before swapping, a = %f, b = %f\n", float1, float2);
    // your code starts here
     float temp = float1; 
    float1 = float2;
    float2 = temp;
    // your code ends here
    printf("after swapping, a = %f, b = %f\n", float1, float2);
    return 0;
}
```

## How to Run Your Code

To run the code, you need to make sure that you are first in the right folder/directory in your terminal (the text area under your code):
Currently, in the example, the user is in the directory `/workspaces/codespaces-blank` you need to get to `/workspaces/codespaces-blank/<homework-repository-name>/hw1` to run your `main.c` code, do this by writing the command `cd <homework-repository-name>/hw1` (cd: change directory) and press enter.

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

Modify `main.c` file inside the `hw1` folder containing the code that does the above. Refer to the [Main README.md](../README.md) for details.


