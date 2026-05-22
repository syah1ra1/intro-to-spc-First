# Generate the boxplot of weight by sex
p_weight_boxplot <- ggplot(bigclass, aes(x = sex, y = weight, fill = sex)) +
  geom_boxplot(outlier.colour = "#D55E00") +
  scale_fill_manual(values = c("F" = "#CC79A7", "M" = "#009E73")) +
  labs(
    title = "Weight Distribution by Sex",
    x = "Sex",
    y = "Weight (lbs)"
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

htmlwidgets::saveWidget(
  plotly::ggplotly(p_weight_boxplot),
  file = file.path("media", "plots", "weight_by_sex_boxplot.html"),
  selfcontained = TRUE
)
