# Generate the scatterplot of height vs weight, colored by sex
p_height_weight_scatter <- ggplot(bigclass, aes(x = height, y = weight, color = sex)) +
  geom_point(alpha = 0.7) +
  scale_color_manual(values = c("F" = "#CC79A7", "M" = "#0072B2")) +
  labs(
    title = "Height vs. Weight, Colored by Sex",
    x = "Height (inches)",
    y = "Weight (lbs)",
    color = "Sex"
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18, face = "bold"),
    axis.title = element_text(size = 18),
    axis.text = element_text(size = 14),
    panel.background = element_rect(fill = "white", colour = NA),
    plot.background = element_rect(fill = "white", colour = NA),
    legend.position = "right"
  )

htmlwidgets::saveWidget(
  plotly::ggplotly(p_height_weight_scatter),
  file = file.path("media", "plots", "height_weight_scatterplot.html"),
  selfcontained = TRUE
)
