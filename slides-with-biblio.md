---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

# Bibliography
<div id="refs"></div>

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores Distribution

This histogram shows the frequency distribution of Math scores in our dataset.

Key observations:
- Most students score between 400 and 600.
- There's a noticeable spread in scores, indicating varying academic performance.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_scores_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores Distribution

This histogram shows the frequency distribution of Math scores in our dataset.

Key observations:
- Most students score between 400 and 600.
- There's a noticeable spread in scores, indicating varying academic performance.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_scores_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores by Gender

This boxplot illustrates the distribution of Math scores separated by gender.

**Observations:**
- The median Math scores appear similar for both genders.
- There might be slight differences in the spread or outliers, suggesting variations in score consistency.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_gender_boxplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores by Gender

This boxplot illustrates the distribution of Math scores separated by gender.

**Observations:**
- The median Math scores appear similar for both genders.
- There might be slight differences in the spread or outliers, suggesting variations in score consistency.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_gender_boxplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Heights

This histogram visualizes the distribution of student heights.

**Observations:**
- The distribution appears to be roughly normal, centered around a particular height range.
- There's a spread indicating natural variation in student heights.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/height_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Heights

This histogram visualizes the distribution of student heights.

**Observations:**
- The distribution appears to be roughly normal, centered around a particular height range.
- There's a spread indicating natural variation in student heights.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/height_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores Distribution

This histogram shows the frequency distribution of Math scores in our dataset.

Key observations:
- Most students score between 400 and 600.
- There's a noticeable spread in scores, indicating varying academic performance.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_scores_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores by Gender

This boxplot illustrates the distribution of Math scores separated by gender.

**Observations:**
- The median Math scores appear similar for both genders.
- There might be slight differences in the spread or outliers, suggesting variations in score consistency.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_gender_boxplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Heights

This histogram visualizes the distribution of student heights.

**Observations:**
- The distribution appears to be roughly normal, centered around a particular height range.
- There's a spread indicating natural variation in student heights.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/height_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Age

This histogram shows the frequency distribution of student ages.

**Observations:**
- The ages are distributed between 12 and 18 years old.
- The most frequent age appears to be around 14-15 years.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/age_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Average Math Score by Sex

This bar chart compares the average Math scores between different sexes.

**Observations:**
- The average Math scores are quite similar for both males and females.
- There might be slight differences, but they are not very pronounced in this dataset.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/avg_math_by_sex_bar.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Weight Distribution by Sex

This boxplot illustrates the distribution of student weights, grouped by sex.

**Observations:**
- There are clear differences in median weight between males and females.
- The spread of weights also varies between the groups.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/weight_by_sex_boxplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Height vs. Weight, Colored by Sex

This scatterplot visualizes the relationship between height and weight, with points colored by sex.

**Observations:**
- A positive correlation between height and weight is observed.
- There are distinct clusters for males and females, indicating differences in height-weight distributions between sexes.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/height_weight_scatterplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores Distribution

This histogram shows the frequency distribution of Math scores in our dataset.

Key observations:
- Most students score between 400 and 600.
- There's a noticeable spread in scores, indicating varying academic performance.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_scores_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores by Gender

This boxplot illustrates the distribution of Math scores separated by gender.

**Observations:**
- The median Math scores appear similar for both genders.
- There might be slight differences in the spread or outliers, suggesting variations in score consistency.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_gender_boxplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Heights

This histogram visualizes the distribution of student heights.

**Observations:**
- The distribution appears to be roughly normal, centered around a particular height range.
- There's a spread indicating natural variation in student heights.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/height_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Distribution of Age

This histogram shows the frequency distribution of student ages.

**Observations:**
- The ages are distributed between 12 and 18 years old.
- The most frequent age appears to be around 14-15 years.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/age_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Average Math Score by Sex

This bar chart compares the average Math scores between different sexes.

**Observations:**
- The average Math scores are quite similar for both males and females.
- There might be slight differences, but they are not very pronounced in this dataset.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/avg_math_by_sex_bar.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Weight Distribution by Sex

This boxplot illustrates the distribution of student weights, grouped by sex.

**Observations:**
- There are clear differences in median weight between males and females.
- The spread of weights also varies between the groups.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/weight_by_sex_boxplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Height vs. Weight, Colored by Sex

This scatterplot visualizes the relationship between height and weight, with points colored by sex.

**Observations:**
- A positive correlation between height and weight is observed.
- There are distinct clusters for males and females, indicating differences in height-weight distributions between sexes.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/height_weight_scatterplot.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

:::: {.columns}
::: {.column width="50%"}
### Math Scores Distribution

This histogram shows the frequency distribution of Math scores in our dataset.

Key observations:
- Most students score between 400 and 600.
- There's a noticeable spread in scores, indicating varying academic performance.

:::

::: {.column width="50%"}
<iframe
  data-src='media/plots/math_scores_histogram.html'
  width='100%'
  height='500px'
  style='border:none;'
  scrolling='no'>
</iframe>
:::
::::

----

---
# Bibliography
<div id="refs"></div>
