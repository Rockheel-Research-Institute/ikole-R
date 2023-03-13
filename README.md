This repo contains C++ codes, libraries and a Rcpp wrapper around them compiled into a R software package.

Through the package, you can inference popular open source ML models "Whisper", "LLAMA" e.t.c. in R. 

It is built to run straight out of box on CPU i.e. no need for external C or C++ libraries or additional installation.

GPU support may be provided in the future. 

It leverages Rcpp for efficient implementation.

Available models:

Whisper
Stable diffusion
LLAMA
GPT-J  
GPT-3  



Examples:

Acknowledgements:

Georgi Gerganov - link ()



Steps:

1. Download model weights (could be in different formats): e.g.  from huggingface  e.t.c.

2. Convert model weights to ggml class (which has been optimized for efficiency on a CPU)

3. Push weights and input file into C/C++ (or push prompts into C/C++)

4. Run the model on the input using optimized functions from ggml class

5. Pull result back to R


WHISPER:

1. whisper.R  (Download model, Call RCpp)

2. convert-pt-to-ggml.py  (Converting script)

3. rcpp_whisper.cpp (Push weights and model into Cpp)

4. whisper.cpp  (Run model)

5. rcpp_whisper.cpp (Pull result back into R)





