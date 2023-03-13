
## Clean up ggml.c for CRAN compliance
x<-readLines("../ikole-R/C/ggml.c")
x <- x[-grep(pattern = "abort()", x)]
x <- c('#include "R.h"', x)
x <- gsub(x, pattern = "fprintf(stderr, ", replacement = "Rf_error(", fixed = TRUE)
x <- gsub(x, pattern = "printf(__VA_ARGS__)", replacement = "Rprintf(__VA_ARGS__)", fixed = TRUE)
#writeLines(x, "src/whisper_cpp/ggml.c")
writeLines(x,"../ikole-R/C/ggml.c")

## Clean up whisper.cpp for CRAN compliance
x<- readLines("../ikole-R/C++/Whisper/whisper.cpp")
x <- c('#include <Rcpp.h>', x)
x <- gsub(x, pattern = "fprintf(stderr, ", replacement = "Rprintf(", fixed = TRUE)
x <- gsub(x, pattern = " printf(", replacement = " Rprintf(", fixed = TRUE)
x <- gsub(x, pattern = "fflush(stdout)", replacement = "Rcpp::checkUserInterrupt()", fixed = TRUE)
writeLines(x, "../ikole-R/C++/Whisper/whisper.cpp")

