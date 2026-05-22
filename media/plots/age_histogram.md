# Generate the histogram of ages
p_age_hist <- ggplot(bigclass, aes(x = age)) +
  geom_histogram(binwidth = 1, fill = "#D55E00", color = "white") +
  labs(
    title = "Distribution of Age",
    x = "Age",
    y = "Frequency"
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18, face = "bold"),
    axis.title = element_text(size = 18),
    axis.text = element_text(size = 14),
    panel.background = element_rect(fill = "white", colour = NA),
    plot.background = element_rect(fill = "white", colour = NA)
  )

htmlwidgets::saveWidget(
  plotly::ggplotly(p_age_hist),
  file = file.path("media", "plots", "age_histogram.html"),
  selfcontained = TRUE
)
