# InsightIDQA
I worked on a consulting project with the company Insight Data Science on their goal to preserve valuable data science related information from Alumni in the form of questions/answers. Insight Data Science is a company that provides a 7-week postdoctoral training fellowship to bridge the gap between academics and data science. With an existing network of over 1200 data science professionals with direct experience solving problems at top companies, the information shared from Insight alumnis is a rich untapped resource that can be a tool to help produce better future Insight fellows. Due to the large volume of messages, my objective as a first pass at this problem is to build a model that can classify relevant data science content from non-data science related messages.

## Data Exploration
I used a simple heuristic to look for messages that began with question type words like why, what, where, should and so forth to look at data science content from different Slack channels. A cursory look, shows that example messages from the general channel were largely social while the messages from the data science channels were more informative. Other channels titled beer or hiking for example included messages that were unrelated to data-science. I then made the decision to aggregate data science related channels and label those messages as data science versus if they were from the general channel. See the Exploratory notebook for code.

The data were in the form of json files containing roughly ~90,000 unlabeled messages grouped by day. I took a subset of those messages and used natural language processing tool kit to do text-cleaning and pre-processing before applying a TF-IDF vectorization of features in order to explore the data and build my classifier. Exploratory analyses showed that there was an order of magnitude more of messages compared to the data-science channels. There are also similar word choices shared between the two. Perhaps regulating channel usage and channel creation would allow for more effective data collection in the future.

## Moving Forward
Insight data science can use this classifier to filter out irrelevant content and preserve valuable data science questions and answers that have been provided by industry experts. Streamlining access to this high-value content will ultimately help the company to produce better data scientists and advance the work of professional data scientists within the Insight alumni community. In addition to this classifier, I also provide useful suggestions for more effective channel use moving forward to improve over time and a code base that will allow this project to be carried forward by data scientists within the organization.

* A subset of Slack data cleaned and ready in an easy to analyze format
* A simple heuristic to look for messages that began with question type words like why, what, where should and so forth
* Built a classifier to filter out extraneous information unrelated to data science for future use

To get the full repo, please contact Insight Data Science as this is only preliminary version. 
