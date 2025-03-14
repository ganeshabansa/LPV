# How to run practicals

## HPC Practicals
### For running openmp programs run commands:-
### Option-1
`g++ filename.cpp -fopenmp` and `./a.exe` [for windows users] or `./a.out` [for linux users]

### Option-2
`g++ -fopenmp filename.cpp -o executable`
`./executable`
 
 [Make sure MinGW is installed with pthreads](https://stackoverflow.com/a/39256203).
 
If you still get errors try running: `mingw-get upgrade --recursive "gcc<4.7.*" "gcc-g++<4.7.*"`


### To run CUDA programs on Collab, follow these steps:
1. [Go to Google Collab](https://colab.research.google.com)
2. Create a new Notebook(.ipynb file).
3. Click on Runtime and change runtime type to GPU.
4. Now run `!pip install git+https://github.com/afnan47/cuda.git` in a cell.
5. On a new cell run `%load_ext nvcc_plugin`
6. Test the following code
```
%%cu
#include <iostream>
int main(){
  std::cout << "Hello World\n";
  return 0;
}
```

7. Remember to add `%%cu` before writing the C++ code for every CUDA program. CUDA is now set.
