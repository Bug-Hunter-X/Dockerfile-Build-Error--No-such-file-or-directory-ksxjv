# Dockerfile Bug: Missing requirements.txt

This repository demonstrates a common error in Dockerfiles: attempting to copy a file that doesn't exist in the build context.  The original Dockerfile tries to install dependencies using `pip3 install -r requirements.txt`, but the `requirements.txt` file is not included in the build context.  The solution demonstrates the correct way to handle this situation.

## Original Dockerfile (bug.Dockerfile)
The original Dockerfile is located in `Dockerfile`. It will fail to build due to the missing requirements.txt file.

## Solution (Dockerfile_solution)
The solution is located in `Dockerfile_solution`. It includes the `requirements.txt` file in the build context before attempting to install the dependencies.
