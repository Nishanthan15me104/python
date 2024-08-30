# The Analysis 

## what are the most in demand skills for the top three most popular roles?

To find the most demanded skills for the top 3 most popular data roles. I filtered out those positions by which ones were the most popular, and got the top 5 skills for these top 3 roles. This query highlights the most popular job titles and their top skills, showing which skills I should pay attention to depending on the role I'm targeting.

View my notebook with detailed steps here:
[skill_count.ipynb](3.Project/2.Skill_count.ipynb)

### Visualize Data 


    fig, ax =plt.subplots(len(job_titles), 1)

    for i, job_title in enumerate(job_titles):

        df_plot = df_skill_count[df_skill_count['job_title_short'] == job_title].head(5) 
        df_plot.plot(kind='barh',y='skill_count',x='job_skills',ax=ax[i],title =job_title)
        ax[i].invert_yaxis
        ax[i].set_ylabel('')
        ax[i].legend().set_visible(False)

    fig.suptitle('Count of Top_Skill in Job_posting', fontsize=15)

    plt.show()


### Results
![3.Project/Images/skill_demand.png)


### Insights

- Python and SQL are essential across all three roles, with Python being especially crucial for Data Scientists.

- SQL is critical for both Data Analysts and Data Engineers, reflecting its foundational role in data-related tasks.

- Data Engineers have a diverse set of required skills, including cloud platforms like AWS and Azure

- Visualization tools like Tableau and Power BI are more relevant for Data Analysts, while Data Scientists and Data Engineers focus more on programming languages and cloud services.

