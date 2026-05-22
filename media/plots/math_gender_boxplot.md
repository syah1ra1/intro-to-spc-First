# Generate the boxplot of Math scores by Gender
p_boxplot <- ggplot(bigclass, aes(x = sex, y = Math, fill = sex)) +
  geom_boxplot(outlier.colour = "#D55E00") +
  scale_fill_manual(values = c("F" = "#0072B2", "M" = "#009E73")) +
  labs(
    title = "Math Scores Distribution by Gender",
    x = "Gender",
    y = "Math Score"
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18, face = "bold"),
    axis.title = element_text(size = 18),
    axis.text = element_text(size = 14),
    panel.background = element_rect(fill = "white", colour = NA),
    plot.background = element_rect(fill = "white", colour = NA),
    legend.position = "none"
  )

# Save the plot as an HTML widget
htmlwidgets::saveWidget(
  plotly::ggplotly(p_boxplot), 
  file = file.path("media", "plots", "math_gender_boxplot.html"),
  selfcontained = TRUE
)
