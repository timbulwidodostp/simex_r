# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Simulation extrapolation (Simex) Use simex With (In) R Software
install.packages("simex")
library("simex")
simex_r = read.csv("https://raw.githubusercontent.com/timbulwidodostp/simex_r/main/simex_r/simex_r.csv",sep = ";")
# Estimation Simulation extrapolation (Simex) Use simex With (In) R Software
y <- simex_r$y
x <- simex_r$x
w <- simex_r$w
true.model <- lm(y~x)
naive.model <- lm(y~w, x=TRUE)
simex.model <- simex(model = naive.model, SIMEXvariable = "w" , measurement.error= 25)
summary(simex.model)
plot(simex.model, mfrow = c(2,2))
# Simulation extrapolation (Simex) Use simex With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished