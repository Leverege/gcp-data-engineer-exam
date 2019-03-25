# Google Cloud - Professional Data Engineer Exam Study Materials
Several engineers at Leverege recently studied for and passed the [Google Cloud Professional Data Engineer](https://cloud.google.com/certification/data-engineer) certification exam. The exam not only covers Google's flagship big data and machine learning products (e.g. BigQuery, BigTable, Cloud ML Engine), but also tests you on your ability to analyze and design for data engineering problems. While we had experience with many of the GCP products tested on the exam, more studying was necessary to encompass the entire scope of the exam. We have put together a [collection of study materials](https://github.com/Leverege/gcp-data-engineer-exam/blob/master/Data%20Engineering%20Notes.pdf) that we used to prepare for the exam. We hope that our study guides help you pass your exam on your first try! 

## Exam Format
Google Cloud Professional Data Engineer Exam consists of 50 multiple choice questions. You have two hours to complete the exam at a certified test location. It's important to note that paper and pencils are not allowed in the exam. We highly suggest going through the [official practice exam](https://cloud.google.com/certification/practice-exam/data-engineer) without writing anything down to simulate an actual test environment. Some questions will ask you to pick multiple answers, but the prompt will also let you know how many correct answers there are. For example, there may be a question on what types of machine learning algorithms you can use to given a dataset, and given six choices, you pick three correct options. 

We found the official practice exam to be similar in difficulty as the actual exam. The practice test included at the end of [Preparing for the Google Cloud Professional Data Engineer Exam](https://www.coursera.org/learn/preparing-cloud-professional-data-engineer-exam) on Coursera was also helpful to see what types of questions might be asked. We also took the 50-question practice exam on the [Linux Academy course](https://linuxacademy.com/google-cloud-platform/training/course/name/google-cloud-data-engineer), but found it a bit misleading in terms of question style. A sample LinuxAcademy question might ask what GCP product to use when you have an existing Hadoop cluster, but most of the actual exam questions had a customer scenario and focused on designing the solution rather than simply picking a product. It was still good a resource to gauge your pace, however, as the other practice tests are only 25 questions each. 

## Study Plan
Since this is a GCP Data Engineering exam, it's imperative to know the key GCP products. It's best to get hands on experience by completing the [Data Engineering track](https://google.qwiklabs.com/quests/25) on Qwiklabs, but if you are pressed for time, you can read our Data Engineering Notes or other cheatsheets compiled by [jorwalk](https://github.com/jorwalk/data-engineering-gcp/blob/master/study-guide.md) and [ml874](https://github.com/ml874/Data-Engineering-on-GCP-Cheatsheet).

Once you are familiar with the GCP products, it's good to study up on the Hadoop ecosystem (e.g. Hadoop, Hive, Spark) and its GCP equivalent as well as key ML concepts. There were no in depth questions on TensorFlow, machine learning, or deep neural networks, but the exam did test on feature engineering strategies (e.g. how to combat overfitting) and identifying potential machine learning questions to solve. 

There were several questions on the two case studies listed on the [website](https://cloud.google.com/certification/guides/data-engineer/) (i.e. Flowlogistic, MJTelco), but the questions did not require you to re-read the actual case study again during the exam. All of the information needed to answer the question regarding the case studies was embeded within the question itself. We suggest going through the video on the Coursera course to dissect the case studies, but not memorize or over analyze this portion too much. 

Overall, there was a heavy emphasis on design, troubleshooting, and optimization of various data engineering scenarios. A common type of problem was asking how to re-design an existing solution at scale or implementing a fix given issues in the current architecture. 

For example:
1) A current Cloud SQL implementation has a single table with a few data points. In the future, if the throughput is 100x higher, how can you partition/shard the tables to improve performance?
2) You need to design a global e-commerce application to that can deal with multiple customers trying to buy the same item around the same time. How do you deal with out of order data? 
3) A BigQuery command is taking too long to read/compute/write. How do you change your query to fix this?

There were also a fair number of IAM-related questions, consistent with the types of questions on the practice exam. It was really helpful to review all the IAM roles per product, knowing the different role types assigned to a human user vs a Service Account, and encryption strategies:

1) Give an external consultant access to DataFlow/BigQuery/BigTable, what role would you assign without giving access to the actual data?
2) Customer wants to encrpyt data at rest, but doesn't want to store the keys on GCP. Where should you create keys, and how do you encrypt that data? 

Finally, not all questions were scenario-based. There were a fair number of questions simply asking for product specific details that tested on core concepts of GCP products:

1) How to design the BigTable index to improve performance. 
2) How to avoid exploding index problem for DataStore.
3) What combination of GCP products to use for streaming data and storage.
4) Given technical requirements, what open-source Hadoop products to use to process/store data. 

Each exam probably draws from a larger pool of questions so it's hard to be definitive about what topics to study more, but it's fair to expect more questions on BigQuery, Machine Learning, BigTable, and DataFlow than Cloud SQL, PubSub, or Stackdriver. Some members on our team mentioned a question or two about regulatory requirements (e.g. HIPAA, GDPR), but nothing too specific. 

We hope that the [exam study guide](https://github.com/Leverege/gcp-data-engineer-exam/blob/master/Data%20Engineering%20Notes.pdf) we prepared and used also helps you pass the test. If you notice any inaccuracies or want to contribute, feel free to leave a issue! 

## Resources
Cheatsheets:
- https://github.com/jorwalk/data-engineering-gcp/blob/master/study-guide.md
- https://github.com/ml874/Data-Engineering-on-GCP-Cheatsheet 
- https://medium.com/google-cloud/a-tensorflow-glossary-cheat-sheet-382583b22932 
- https://www.slideshare.net/GuangXu5/gcp-data-engineer-cheatsheet 

Other Exam Overviews/Debriefs:
- https://medium.com/@simonleewm/a-study-guide-to-the-google-cloud-professional-data-engineer-certification-path-9e83e41e311
- https://www.linkedin.com/pulse/google-cloud-certified-professional-data-engineer-writeup-rix/

Courses:
- https://linuxacademy.com/google-cloud-platform/training/course/name/google-cloud-data-engineer 
- https://www.coursera.org/learn/preparing-cloud-professional-data-engineer-exam
- https://google.qwiklabs.com/quests/34
- https://google.qwiklabs.com/quests/25
