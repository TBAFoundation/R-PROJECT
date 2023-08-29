# loading Palmer penguins library for R built in data set
library(palmerpenguins)
# loading ggplot2 library for visualization
library(ggplot2)
# plotting ggplot without data set
ggplot()
# visualizing penguins data set
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g))
# visualizing penguins data set with scatter plot
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point()
# visualizing penguins data set adding color
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point(color = "purple")
# visualizing penguins data set adding color to each species in the data set
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point(aes (color = species))
# visualizing penguins data set adding shape
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point(aes (shape = species))
# visualizing penguins data set adding both shape and color
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point(aes (shape = species, color = species))
# visualizing penguins data set adding faces function to create separate plot for each species
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point(aes (shape = species, color = species))+facet_wrap(~species)
# adding title to our plot
ggplot(data=penguins,aes(x=flipper_length_mm,y=body_mass_g)) + geom_point(aes (shape = species, color = species))+facet_wrap(~species) + labs(title = "Palmer Penguins: Body Mass VS Flipper Lenght")