## honour user .Rprofile
if (file.exists(Sys.getenv("R_PROFILE_USER"))) {
  source(Sys.getenv("R_PROFILE_USER"))
} else if(file.exists(path.expand("~/.Rprofile"))) {
  source(path.expand("~/.Rprofile"))
}

message("packrat project - enabling may take some time")
#### -- Packrat Autoloader (version 0.4.8-54) -- ####
source("packrat/init.R")
#### -- End Packrat Autoloader -- ####
