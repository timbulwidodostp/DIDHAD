# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Heterogeneity-robust DID estimator in heterogeneous adoption designs without stayers but with some quasi-stayers Use did_had (DIDHAD) With (In) R Software
# Estimates the effect of a treatment on an outcome in a heterogeneous adoption design with no stayers but some quasi stayers 
# (see de Chaisemartin and D'Haultfoeuille (2024)) Use did_had (DIDHAD) With (In) R Software
install.packages("DIDHAD")
install.packages("readxl")
install.packages("httr")
library("DIDHAD")
library("readxl")
library("httr")
# Estimation Heterogeneity-robust DID estimator in heterogeneous adoption designs without stayers but with some quasi-stayers Use did_had (DIDHAD) 
# With (In) R Software
# Estimates the effect of a treatment on an outcome in a heterogeneous adoption design with no stayers but some quasi stayers
# (see de Chaisemartin and D'Haultfoeuille (2024))  Use did_had (DIDHAD) With (In) R Software
github_link <- "https://github.com/timbulwidodostp/DIDHAD/raw/main/DIDHAD/DIDHAD.xlsx"
temp_file <- tempfile(fileext = ".xlsx")
req <- GET(github_link, authenticate(Sys.getenv("GITHUB_PAT"), ""), write_disk(path = temp_file))
DIDHAD <- readxl::read_excel(temp_file)
summary(did_had(df = DIDHAD, outcome = "y", group = "g", time = "t", treatment = "d", effects = 5, placebo = 4, kernel = "tri", graph_off = TRUE))
# Heterogeneity-robust DID estimator in heterogeneous adoption designs without stayers but with some quasi-stayers Use did_had (DIDHAD) With (In) R Software
# Estimates the effect of a treatment on an outcome in a heterogeneous adoption design with no stayers but some quasi stayers 
# (see de Chaisemartin and D'Haultfoeuille (2024)) Use did_had (DIDHAD) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished