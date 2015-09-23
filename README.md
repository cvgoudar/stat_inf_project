## Central Limit Theorem : Experimentation with Exponential distribution

### Overview
   In this exercise the central limit theorem is demonstrated with samples from exponential distribution
### Simulations: Include English explanations of the simulations you ran, with the accompanying R code. Your explanations should make clear what the R code accomplishes.
```{r}
n <- 1000
lambda <- 0.2
rexp_pop <- rexp(n, lambda)
rpop_mean <- mean(rexp_pop)
rpop_sd   <- sd(rexp_pop)
hist(rexp_pop)
```



```{r}
# Sampling
# Extract 40 samples from the population mean
samp_mean <- NULL
samp_sd   <- NULL
for (i in 1:1000)
{
  rsamp <- sample(rexp_pop, 40, replace = TRUE)
  samp_mean[i] <- mean(rsamp)
  samp_sd[i]   <- sd(rsamp)
}
hist(samp_mean)
hist(samp_sd)
```

### Sample Mean versus Theoretical Mean: Include figures with titles. In the figures, highlight the means you are comparing. Include text that explains the figures and what is shown on them, and provides appropriate numbers.
### Sample Variance versus Theoretical Variance: Include figures (output from R) with titles. Highlight the variances you are comparing. Include text that explains your understanding of the differences of the variances.
### Distribution: Via figures and text, explain how one can tell the distribution is approximately normal.
