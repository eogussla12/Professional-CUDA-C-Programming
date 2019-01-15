Professional-CUDA-C-Programming

chapter2

#Defining an error-handling macro to wrap all CUDA API calls simplifi es the error checking
process:

#define CHECK(call) 

{

const cudaError_t error = call; 

if (error != cudaSuccess) 

{ 

printf("Error: %s:%d, ", __FILE__, __LINE__); 

printf("code:%d, reason: %s\n", error, cudaGetErrorString(error)); 

exit(1);

} 

}
