# Generate the histogram of heights
p_height_hist <- ggplot(bigclass, aes(x = height)) +
  geom_histogram(binwidth = 2, fill = "#CC79A7", color = "white") +
  labs(
    title = "Distribution of Heights",
    x = "Height (inches)",
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

# Save the plot as an HTML widget
htmlwidgets::saveWidget(
  plotly::ggplotly(p_height_hist), 
  file = file.path("media", "plots", "height_histogram.html"),
  selfcontained = TRUE
)
