# FUTURE_DS_03
Future Interns internship Task 3

Student Event Feedback Analysis Report
1. PROJECT OBJECTIVE
         The objective of this project is to analyze student feedback collected after various college events such as workshops, seminars, technical fests, and cultural activities. The goal is to uncover satisfaction trends using numerical ratings and text comments so that organizers can enhance the planning and delivery of future events.
   The study focuses on:
        Cleaning and preparing survey data
        Analyzing student ratings (1–10 scale)
        Understanding student opinions through sentiment analysis
        Visualizing the distribution of satisfaction levels
        Identifying areas of improvement
        Generating insights and actionable recommendations
   This analysis will help event coordinators understand what students value the most and where improvements are needed.

2. DATASET USED
   The dataset used is: student_feedback.csv (This file was provided as part of the task.)
   Dataset Features
        The dataset contains the following key numerical feedback columns:
        well_versed – Subject knowledge of the instructor
        explains_well – Clarity of explanation
        presentations – Usefulness of presentation materials
        assign_difficulty – Difficulty level of assignments
        solves_doubts – Instructor’s willingness to clear doubts
        course_structure – Quality of course/event structure
        support – Additional support provided
        recommendation – Likelihood of recommending the event
   Synthetic Added Columns (for NLP parts)
        Since the dataset did not contain text comments, a feedback_text column of realistic student comments was generated to enable:
        Sentiment analysis
        Word cloud
        Keyword frequency insights
   Additional Derived Columns
        From the analysis we created:
        overall_score – Mean of all ratings
        satisfaction_level – High / Medium / Low segmentation
        sentiment_score – VADER sentiment value
        sentiment_label – Positive / Neutral / Negative
        event_type – Synthetic event-type labels for group comparison

3. PROCESS (STEP-BY-STEP ANALYSIS)
  Step 1: Data Cleaning
      Removed unnamed columns
      Renamed long question titles into simpler names
      Converted all rating fields to numeric
      Removed rows with missing rating values
      Added synthetic event_type and feedback_text columns
  Step 2: Descriptive Statistics
      Computed mean, median, and standard deviation of all rating columns
      Identified highest and lowest-rated aspects
  Step 3: Visual Analysis
      Generated multiple plots including:
      Average rating bar chart
      Likert-style heatmap of all responses
      Overall satisfaction distribution
      Correlation heatmap
      Variability plot (standard deviation)
      Radar chart of overall rating profile
      Satisfaction-level heatmap (Low vs Medium vs High)
      Event-type boxplot
  Step 4: Sentiment Analysis
      Using VADER, each synthetic student comment was classified as:
          Positive
          Neutral
          Negative
      Visuals included:
          Sentiment distribution bar chart
          Word cloud
          Keyword frequency bar chart
  Step 5: Derived Insights
      Analyzed which rating factors correlate strongly with overall satisfaction
      Compared satisfaction across event types
      Compared ratings across satisfaction levels
      Identified top positive and negative feedback themes

4. DASHBOARD / VISUAL SUMMARY
    The Colab notebook contains a set of interactive and static visualizations that function as the project dashboard:
    Key Visual Components
        Average Rating Plot
        Overall Satisfaction Histogram
        Likert Heatmap
        Correlation Heatmap
        Satisfaction Segmentation
        Radar Chart of Overall Ratings
        Sentiment Distribution
        Word Cloud of Comments
        Keyword Frequency Chart
        Event-Type Satisfaction Comparison
    Together, these visual elements provide a comprehensive dashboard for evaluating student feedback.

5. PROJECT INSIGHTS
1. Overall Satisfaction
    The majority of students fall into the Medium or High satisfaction levels.
    Very few students reported Low satisfaction.
2. Highest Rated Aspects
    solves_doubts
    well_versed
    support
   These indicate strong instructor effectiveness and student interaction quality.
3. Lowest Rated Aspects
    assign_difficulty
    presentations
    Students found assignments challenging and presentations slightly less impactful.
4. Sentiment Insights (from synthetic text)
    Majority of comments were Positive, highlighting:
      Clear explanations
      Helpful instructors
      Engaging workshops
    Negative comments emphasized:
      Fast pace of sessions
      Difficult assignments
      Need for more practical activities
5. Strongest Correlations with Overall Satisfaction
    solves_doubts → highest correlation
    explains_well → second highest
    support → notable influence
  This suggests interpersonal teaching qualities drive satisfaction more than materials.
6. Rating Variability
   “assign_difficulty” had the highest standard deviation, meaning students had mixed opinions about assignment difficulty.
7. Event-Type Differences (Using synthetic event type)
    Workshops received the highest satisfaction overall
    Seminars and cultural events showed moderate satisfaction
    Tech fests showed more variability

6. FINAL CONCLUSION
    This analysis successfully uncovered key satisfaction trends using survey data. Students generally appreciate clear explanations, supportive instructors, and structured events. However, improvements are needed in presentation materials and assignment difficulty levels.

Outcome
    This project demonstrates how simple survey data can be transformed into actionable insights through:
        Data cleaning
        Exploratory data analysis
        Visualization
        NLP-based sentiment analysis
        It fulfills the internship requirement by providing meaningful recommendations to improve student experiences during future events.
