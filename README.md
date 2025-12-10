# VR Data Visualization Project  
A multidataset breakdown of VR engagement, comfort, and user patterns

---

## Abstract

This project pulls together several independent VR datasets and turns them into a connected visualization system that helps explain how real people experience virtual reality. Instead of treating demographic data, headset usage, immersion scores, and assistive technology availability as separate stories, I combined them into one interactive environment using D3.js.

The goal is simple. Understand what makes VR comfortable, what makes it uncomfortable, and how those factors shift depending on who you are and what you are using. The project uses scatter plots, radar charts, icon based filters, and responsive tooltips to create a clear picture of VR usage patterns across multiple populations. This work is both a technical demonstration and a practical exploration of how design and data can work together to support better VR decisions.

---
---

## At a Glance

**Tech Stack**  
- D3.js  
- JavaScript  
- CSV based data pipeline  
- VizHub for hosting and rendering  

**Core Visuals**  
- Engagement scatter plot  
- Users demographic bar chart  
- Three headset comparison panels  
- Gender based radar chart  
- Assistive technology regional view  

**Key Metrics Tracked**  
- Immersion level  
- Motion sickness  
- Session duration  
- Gender patterns  
- Headset differences  
- Engagement levels in education  
- Regional training access  

**Main Questions Answered**  
- How the three headsets differ in comfort and immersion  
- How age and gender shape VR outcomes  
- What usage patterns predict higher immersion or sickness  
- How assistive tech varies across regions  
- How many students use VR and how it affects engagement  

**Project Purpose**  
Turn multiple VR datasets into a unified interactive system that shows how different groups experience VR and why those experiences differ. This project is part research, part visual architecture, and part portfolio ready storytelling.

---

## Introduction

VR is growing fast in entertainment, education, and training, but not everyone experiences it the same way. Some people get immersed. Others get sick. Some groups stay in VR longer and feel more comfortable. Some regions have strong access to assistive technology. Others barely have any.

This project started because I wanted to make sense of all these differences in one place. I imported multiple CSVs, cleaned them, and built out a workflow that connects headset type, gender, age, session duration, motion sickness, immersion, and educational access. From there, I built interactive charts that let me filter, compare, and break down patterns that are not obvious when looking at each dataset alone.

The entire visualization is designed around exploration. You can switch between datasets, filter the visuals by gender or headset, and highlight sections to understand exactly how different groups behave in VR. This project is part research, part portfolio piece, and part personal curiosity about how VR affects people differently.

---

## Project Overview

This project examines how different groups of people experience virtual reality depending on their demographics, hardware choices, and behavioral tendencies. Instead of relying on a single dataset, the analysis synthesizes insights from multiple Kaggle sources covering VR usage, headset adoption, emotional response, consumer behaviors, immersion scores, and accessibility conditions.

The central goal is to understand what factors predict comfort, discomfort, and overall immersion in VR systems. The project uses descriptive visualizations and a structure that can support predictive modeling in later versions to uncover meaningful patterns that shape VR user experience.

---

## Headsets Tracked

The core VR experience dataset focuses on three mainstream headsets:

1. **PlayStation VR**  
2. **HTC Vive**  
3. **Oculus Rift**

These three devices appear consistently in the tree views, headset comparison panels, and radar based visuals.

---

## Research Questions

This project is guided by a set of practical questions. For each one, I note how the current visualizations answer it.

1. **How do the three headsets differ in user demographics, comfort, and immersion**  
   **Answer:** The three panel headset views and VR Experience visual show that PlayStation VR has the largest user base, HTC Vive users tend to have longer sessions with lower motion sickness, and Oculus Rift sits in the middle for both duration and sickness. Demographic splits by gender and age are visible inside the trees and radar chart.

2. **Do age or gender influence motion sickness, immersion, or session duration**  
   **Answer:** The radar chart and headset trees show that younger male users report higher motion sickness, female users tend to stay longer with smoother experiences, and the “Other” gender group has the widest spread due to a smaller sample. Age also shifts the balance of duration and sickness across groups.

3. **What behavioral factors like duration or usage patterns shape comfort and immersion**  
   **Answer:** The duration patterns in the VR Experience views and radar chart show that longer sessions increase both immersion and discomfort. Frequent users appear to adapt over time and report lower motion sickness compared to less frequent users.

4. **Are there geographic differences in assistive technology training and access**  
   **Answer:** The Assistive Technology view highlights strong regional differences. Regions with more resources and infrastructure report more consistent training availability. Under resourced regions show clear gaps.

5. **Which features best predict a positive or negative VR experience if we move into modeling**  
   **Answer:** The current project sets this up rather than fully training models. The visuals suggest that headset type, session duration, age, gender, and prior experience would be core features, because those are the variables that visibly track with comfort, immersion, and reported sickness.

6. **Which headset type appears most often in the dataset**  
   **Answer:** The headset comparison and trees show that PlayStation VR appears most often and has the largest user count in the VR Experience data.

7. **Are there meaningful gender based differences in VR outcomes**  
   **Answer:** Yes. The radar chart shows clear differences between male, female, and other genders in average motion sickness, duration, and immersion, with males skewing toward higher sickness, females toward longer and smoother sessions, and other gender users showing more variability.

8. **Are there noticeable spatial or regional patterns when comparing datasets**  
   **Answer:** The Assistive Technology view and region fields in the education datasets show patterns where more developed regions have better training and access, while other regions show patchy or limited availability.

9. **How do user counts shift across demographic categories such as age group or education level**  
   **Answer:** The Users view grouped bar chart shows how counts change as you move across age bands and education levels. You can see which age groups and levels are most represented and where participation drops off.

10. **How does the United States compare to other regions in assistive technology access**  
    **Answer:** In the Assistive Technology dataset, the United States falls into the higher access category compared to many other regions, matching the broader pattern that higher resource regions report more training availability.

11. **How many students in the education datasets actively use VR in education**  
    **Answer:** The Impact and Modified Education datasets include a `Usage_of_VR_in_Education` flag that lets you filter down to VR students. The Engagement and Users views use this to highlight VR users versus non-users, and visually show that VR users are a focused subset rather than the majority.

12. **What patterns point to higher discomfort or risk in VR use**  
    **Answer:** Higher risk patterns appear where younger users, higher session durations, and certain headset combinations line up with motion sickness scores at the upper end of the scale. These patterns are visible in the VR Experience views and radar chart.

13. **Does headset model correlate with comfort, immersion, or session duration**  
    **Answer:** Yes. The headset comparison views show that HTC Vive is correlated with longer sessions and relatively lower sickness, PlayStation VR has broad adoption with mixed comfort, and Oculus Rift sits in between for comfort and immersion.

The visualizations and interactions in this project are designed to make these questions easier to explore and to surface clear, visual answers.

---

## Data

### Core Project Datasets

These are the main datasets that drive the current visualizations:

1. **Virtual_Reality_in_Education_Impact.csv**  
   Student level VR usage and outcome data.  
   Key columns include:  
   - `Student_ID`  
   - `Age`  
   - `Gender`  
   - `EducationLevel` / `Grade_Level`  
   - `Usage_of_VR_in_Education` (Yes / No)  
   - `Hours_of_VR_Usage_Per_Week`  
   - `Engagement_Level` (1 to 5)  
   - `Improvement_in_Learning_Outcomes` (Yes / No)  
   - `Instructor_VR_Proficiency`  
   - `Region`  

2. **Modified_Virtual_Reality_in_Education_Dataset.csv**  
   Education context and VR implementation details.  
   Key columns include:  
   - `Age`  
   - `EducationLevel`  
   - `Usage_of_VR_in_Education`  
   - `Hours_of_VR_Usage_Per_Week`  
   - `Engagement_Level`  
   - `Improvement_in_Learning_Outcomes`  
   - `Instructor_VR_Proficiency`  
   - `Access_to_VR_Equipment`  
   - `Stress_Level_with_VR_Usage`  
   - `Collab` (collaboration indicator)  

3. **assistive technology.csv**  
   Global assistive technology training availability.  
   Key columns include:  
   - `ParentLocation` (region)  
   - `Location` (country)  
   - `Dim1` (training category)  
   - `Period` (year)  
   - `Value` (availability indicator)  

4. **Virtual Reality Experiences.csv**  
   User experience metrics for the three VR headsets.  
   Key columns include:  
   - `UserID`  
   - `Age`  
   - `Gender` (Male, Female, Other)  
   - `VRHeadset` (PlayStation VR, HTC Vive, Oculus Rift)  
   - `Duration` (minutes)  
   - `MotionSickness` (1 to 10)  
   - `ImmersionLevel` (1 to 5)  

5. **Student math and Portuguese datasets**  
   Standard student demographic and academic performance for comparison and possible modeling.  
   Common columns include:  
   - `student_id`  
   - `sex`  
   - `age`  
   - family and study context  
   - failures and scores  

These datasets are the ones directly used in the views that ship with this project.

---

### Additional Reference Datasets Considered

The project also draws on ideas from other Kaggle datasets, even if not all of them are wired into the current version:

- https://www.kaggle.com/datasets/lumaatabbaa/vr-eyes-emotions-dataset-vreed  
- https://www.kaggle.com/datasets/yapwh1208/availability-of-education-for-assistive-technology  
- https://www.kaggle.com/datasets/leetheoiv/steam-virtual-reality-vr-video-games-dataset  
- https://www.kaggle.com/datasets/szhao2020/vr-gaming-network-traffic  
- https://www.kaggle.com/datasets/programmer3/emotion-recognition-in-mobile-vr-films  
- https://www.kaggle.com/datasets/ilokabenneth/augmented-reality-consumer-behaviour-consumer-enga  

All datasets are sourced from Kaggle.

---

## Methodology

### Data Cleaning and Integration

I standardized columns like engagement level, gender labels, and headset names so the datasets could be combined or compared without confusion. Numeric fields were converted where needed, Yes / No fields were normalized, and scales for hours, engagement, and immersion were aligned.

Once the data was cleaned, I pulled it into a shared D3 based structure so filters and interactions could work the same way across multiple views. The main challenge was dealing with different sample sizes, especially for the Other gender group and regions with fewer assistive technology records.

---

### Visual Architecture

I used the same filtering logic across all visuals so user interactions feel consistent. The main components include:

- Scatter plots showing engagement versus hours of VR usage  
- Grouped bar charts showing user distribution across age and education levels  
- Radar charts showing immersion, duration, motion sickness, and average age by gender  
- Headset filters that update the visuals instantly  
- Gender filters that change the shape of the radar and scatter plots  
- Hover interactions that highlight specific elements and dim the rest  
- Icons and legends placed in clean whitespace outside the main chart area  

The visual system is intentionally modular so it can be extended or reused with new datasets.

---

### Predictive Thinking

While the final project is visualization focused, the structure is ready for future modeling. Features like gender, duration, age, headset type, engagement, and immersion are aligned so they can feed into regression or classification models that predict comfort or risk levels.

---

## Visualizations

### Engagement View

An interactive scatter plot that analyzes the relationship between engagement level and weekly VR usage hours.

- **X-axis:** Engagement Level (1 to 5)  
- **Y-axis:** Hours of VR Usage Per Week  
- **Color:** Dataset source (Impact vs Modified Education)  
- **Fill:** VR users vs non-users  

Interactions:

- Toggle datasets on and off  
- Option to show only VR users  
- Hover tooltips with detailed student level information  

This view connects directly to questions about how usage relates to engagement and which groups cluster at certain engagement levels.

---

### Users View

A grouped bar chart that visualizes user distribution across age ranges and education levels.

- **X-axis:** Age groups in 5 year bands  
- **Y-axis:** Count of users  
- **Color:** Education level (High School, Undergraduate, Postgraduate)  

Interactions:

- Filter by education level  
- Hover to display exact counts  
- Compare bars within each age group  

This helps answer questions about how user counts shift across demographic categories.

---

### Headset Comparison Panels

A three panel spread for the tracked headsets:

1. PlayStation VR  
2. HTC Vive  
3. Oculus Rift  

Each panel shows how users of that headset differ by:

- Motion sickness  
- Immersion level  
- Session duration  
- Demographic patterns  

These views support comparisons of comfort and usage behavior across headsets and feed directly into the headset focused research questions.

---

### Radar Chart

A radar chart that compares average metrics by gender:

- **Metrics:** Average Age, Motion Sickness, Duration, Immersion  
- **Genders:** Male, Female, Other  

Interactions:

- Toggle gender categories on or off  
- Hover on each point to see metric name and exact value  
- Hover near the center to show a summary across all visible genders  

This supports questions about gender based differences in VR outcomes and how demographics shape comfort and immersion.

---

### Assistive Technology View

A view built from the assistive technology dataset that focuses on regional access and training availability.

- Breaks down training availability by region and country  
- Highlights gaps and uneven distribution across regions  
- Connects directly to questions about spatial patterns and where the United States sits relative to other regions  

---

### Impact and Education Charts

These visuals tie VR adoption to engagement and improvements in learning outcomes:

- Compare VR users and non-users  
- Break out results by education level and region  
- Highlight which groups show the strongest improvement when VR is available  

These charts are used to answer questions around how many students use VR and how that relates to engagement and learning improvements.

---

## Key Findings

### Comfort and Discomfort Patterns

- Younger male users show higher motion sickness.  
- Female users tend to stay longer in VR and report smoother experiences.  
- Other gender groups show the widest range in values, partly due to smaller sample sizes.  

These patterns answer questions about how age and gender influence motion sickness, immersion, and duration.

---

### Headset Behavior Differences

- HTC Vive supports longer sessions with lower average sickness.  
- PlayStation VR has the largest user count in the dataset.  
- Oculus Rift tends to sit in the middle for both duration and sickness.  

These findings address how the three headsets differ in comfort and immersion and confirm that headset model does correlate with user experience.

---

### Immersion vs Duration

- Longer sessions increase both immersion and discomfort at the same time.  
- Frequent users adapt to VR and tend to report lower sickness over time.  

These patterns answer questions about behavioral factors and how duration shapes both comfort and immersion.

---

### Geographic Accessibility

- Assistive technology training is uneven globally.  
- Regions with stronger infrastructure and funding report more consistent training availability.  
- Under resourced regions show clear gaps in access.  
- The United States falls into the higher access group when compared to global data.  

These insights answer questions about geographic differences, spatial patterns, and where the United States sits in terms of assistive technology.

---

### Question Coverage Summary

- Headset differences, gender impact, and behavioral factors are covered through the VR Experience, radar chart, and comparison panels.  
- Geographic and regional questions are explored through the assistive technology view.  
- Student adoption and engagement are examined in the education based scatter and bar charts.  
- Risk factors are inferred from combinations of age, duration, sickness, and headset type, with more formal modeling listed as future work.  

---

## Sketches

Before building the final visuals, I sketched several structures that guided the design.

### Risk Factor Tree

Hierarchy showing:

- All users  
- Device  
- Gender  
- Comfort risk level  

This informed the VR Experience tree layout.

---

### Comfort Severity Heatmap

A grid where rows represent headsets and columns represent demographic or behavioral slices. Each cell encodes average discomfort. The final design moved toward trees and radar charts, but this heatmap idea shaped how I grouped metrics.

---

### Predictive Model Flow Diagram

A flow diagram that moves from input features:

- Age  
- Gender  
- Headset  
- Session duration  
- Experience level  

to outputs like:

- Comfort score  
- Immersion rating  
- Risk probability  

The diagram guided how I structured the data and how I think about future modeling.

---

## Project Goals

- Identify what makes VR comfortable or uncomfortable  
- Compare major headset demographics and behavioral patterns  
- Understand how consumer and student behavior relates to VR outcomes  
- Prepare data and structure for predictive models of comfort, immersion, and engagement  
- Produce clear, interpretable visualization prototypes that support exploration and decision making  

---

## Why This Project Matters

VR is rapidly entering entertainment, education, therapy, and accessibility. Understanding user comfort and risk factors is critical if we want healthy, sustainable adoption.

This project matters because it:

- Surfaces real patterns in how different people experience VR  
- Helps developers think about comfort and risk in a structured way  
- Gives educators insight into how VR relates to engagement and outcomes  
- Highlights accessibility and regional gaps that deserve attention  

It also shows how multidataset visualizations can tell a bigger and more honest story than any single dataset on its own.

---

## Prototypes

I have created a set of proof of concept visualizations for this data. These range from scatter plots to hierarchical trees and radar charts.

[![image](https://github.com/fokalview/VR-Data/blob/master/3panel.png)](https://vizhub.com/fokalview/f2e723cc55194e98ab325c524371c4e4)

<div align="center">

### PlayStation VR, HTC Vive, and Oculus Rift 3 Panel Spread

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/PlaystationVR.png)](https://vizhub.com/fokalview/0cc21ddd8b9c403b856b1dbe925a4ab5)

<div align="center">

### PlayStation VR

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/HTC.png)](https://vizhub.com/fokalview/16bb6b65f8894e7383ba5840939508d5)

<div align="center">

### HTC Vive

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/oculus.png)](https://vizhub.com/fokalview/02c750bd8dea4c309fd682feb4ce7470)

<div align="center">

### Oculus Rift

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Assitivetech.png)](https://vizhub.com/fokalview/5325ee30f3aa4482bba707138034e637)

<div align="center">

### Assistive Technology

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/VRExp.png)](https://vizhub.com/fokalview/0b4d4f422e2f4721b963b242b6388e84)

<div align="center">

### VR Experience

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Immerion%20SCore.png)](https://vizhub.com/fokalview/772e7b2285d643cbaab3892a6d7d9300)

<div align="center">

### Impact on Score

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Engagment.png)](https://vizhub.com/fokalview/634ce52577aa4d509d022628e38526c3)

<div align="center">

### Engagement

</div>

---

**Sources**

- [Source – 3 Panel Spread](https://vizhub.com/fokalview/f2e723cc55194e98ab325c524371c4e4)  
- [Source – PlayStation VR](https://vizhub.com/fokalview/0cc21ddd8b9c403b856b1dbe925a4ab5)  
- [Source – HTC Vive](https://vizhub.com/fokalview/16bb6b65f8894e7383ba5840939508d5)  
- [Source – Oculus](https://vizhub.com/fokalview/02c750bd8dea4c309fd682feb4ce7470)  
- [Source – Assistive Tech](https://vizhub.com/fokalview/5325ee30f3aa4482bba707138034e637)  
- [Source – VR Experience](https://vizhub.com/fokalview/0b4d4f422e2f4721b963b242b6388e84)  
- [Source – Impact on Score](https://vizhub.com/fokalview/772e7b2285d643cbaab3892a6d7d9300)  
- [Source – Engagement](https://vizhub.com/fokalview/634ce52577aa4d509d022628e38526c3)  

---

## Open Questions

There are still a few views and ideas that I am experimenting with. Some of these may become part of a future version of the project.

- https://vizhub.com/fokalview/5e0d145e049d46a9ac27ba580bd3d589  
- https://vizhub.com/fokalview/c849b29a34cd452abb20fe62bfea0d9d  
- https://vizhub.com/fokalview/2f7d8ea52aa549028a94af36c2b17d41  
- https://vizhub.com/fokalview/3c0b21fb8d3e435a9f4dcaadc9b2bf2e  

These represent alternate ways to encode similar information or early tests of new ideas.

---

## Milestones

- Built the first scatter plot visual  
- Successfully imported and cleaned multiple CSV documents  
- Iterated the scatter plot into a more meaningful layout tied directly to engagement  
- Designed and implemented the three headset comparison views  
- Added the radar chart and connected it to gender and headset filters  
- Integrated the assistive technology view for regional context  

---

## Future Work

- Build a predictive comfort model using regression or classification  
- Add session frequency and experience level into the main views  
- Expand the radar chart to include more variables such as stress or familiarity  
- Develop a full dashboard that combines all views into one interface for decision makers  
- Compare VR data with AR datasets for a more complete picture  
- Add time based analysis where datasets support it, especially for adoption trends  

The architecture is already set up for expansion. The next step is deeper modeling and more refined interaction design.

---

## Project Links

### VizHub Projects  

(Insert final list of URLs or keep the links listed above in Prototypes and Open Questions.)

### GitHub Repository  

https://github.com/fokalview/VR-Data

---

## Conclusion

After combining all these datasets and building out the visuals, the patterns became clear. VR is not a one size fits all experience. Different headsets, demographics, and educational contexts all shape how people feel in virtual environments.

This project helped me understand those patterns in a structured way and strengthened my skills in D3, JavaScript, data cleaning, and visual architecture. It also proved that interactive data work can reveal insights that static charts will always miss.

This is version one. There is more I want to build, but the foundation is solid and the insights are real.
