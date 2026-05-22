# Calculate average Math score by sex
avg_math_by_sex <- bigclass %>% 
  group_by(sex) %>% 
  summarise(avg_math = mean(Math))

p_avg_math_bar <- ggplot(avg_math_by_sex, aes(x = sex, y = avg_math, fill = sex)) +
  geom_bar(stat = "identity") +
  scale_fill_manual(values = c("F" = "#0072B2", "M" = "#009E73")) +
  labs(
    title = "Average Math Score by Sex",
    x = "Sex",
    y = "Average Math Score"
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
  plotly::ggplotly(p_avg_math_bar),
  file = file.path("media", "plots", "avg_math_by_sex_bar.html"),
  selfcontained = TRUE
)
