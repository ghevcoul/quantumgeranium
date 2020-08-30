---
layout: page
title: About me
subtitle: A whirlwind tour through my career
slug: about-me
---

I came to a career in tech and living in California via a rather circuitous route.
Having grown up in Vermont, I chose to move north to do my undergraduate in chemistry a Bishop's University in the Eastern Townships of Quebec.
While studying chemistry, I used nearly all my electives to take computer science courses, ending up a few shy of completing a minor.
I quickly came to realize that I didn't particularly enjoy experimental chemistry (nor was I very good at it, as my lack of fingerprints for most of my 20s will attest), but I still had a great experience in the Bishop's chemistry department.
It is a small department, only four to five professors, and that was I needed at that point in my life.
Coming to university from a town of less than 1000 people and a graduating high school class of 150 drawn from a half dozen towns, I know I would have gotten lost in large program and lectures as large as my high school.
At Bishop's, every professor in the department knew me by the end of my first year and I flourished under their guidance and support.

As I was completing my bachelors degree, my professors pointed me toward [computational chemistry](/blog/gay-lussac-kohn-pople) for grad school, knowing that it would be a good fit.
This led me to the research group of the inimitable [Russ Boyd](https://www.dal.ca/faculty/science/chemistry/faculty-staff/our-faculty/emeritus-professors/russell-boyd.html) at Dalhousie University in Halifax, Nova Scotia.
This turned out to be exactly what I wanted, both the research experience and the city.
I loved living in Halifax - the people, the food, the ocean, the walkability.
Additionally, I loved the experience of working in computational sciences research.
This was my first experience using the high performance computing clusters, which I don't think gets enough recognition in industry as another form of distributed cloud computing.
I quickly became comfortable spending most of my day on the command line SSHed into remote systems that might be in the next room or the other side of the continent.
Everything I could automate about my work with bash scripts I did - I still live by the guiding principle of trying to automate myself out of every job I have.
When I ran up against the limitations of bash scripting, I learned Python and was able to push my work even further.
Moreover, I learned quantum chemistry and was reminded of why I chose to study chemistry in the first place.
In high school chemistry, it was never the lab work the prompted me to major in it, but the deep understanding of [how the world around me works](/blog/salted-water).
Quantum mechanics and a deeper understanding of the atomistic world gave me a whole new appreciation for the sciences.
Even though I now haven't worked in chemistry for six years, not a day goes by that I don't look at some aspect of my life through that lens.

Coming out of my PhD, I was certain that I wanted to follow a career in academia, so I did the next sensible thing and started a postdoctoral fellowship with [Nick Mosey](http://moseygroup.ca/index.html) at Queen's University.
This continued my work in computational chemistry, albeit this time with a more materials science focus.
Moreso than then chemistry I was doing, my postdoc gave me yet another opportunity to grow as a software developer.
My research group did all their work with an open source simulation package called [Quantum ESPRESSO](https://www.quantum-espresso.org/) and frequently made modifications to support new research.
As I did my project, we came across a paper detailing a new simulation technique that was perfect for what I needed to do, but hadn't been added to Quantum ESPRESSO yet, so I got to spend a few months digging into this large Fortran codebase and implement this new method.
The other major thing that happened while doing my postdoc (other than meeting my wonderful spouse, that is) was that I came to realize an academic career wasn't what I wanted.

This was late 2014, when data science was exploding in tech and there were pieces being written daily about data as the next oil boom and how any company that wasn't building a data team was going to be left behind.
Looking at all this, I realized that I was exactly the kind of person these articles said was becoming data scientists -- advanced degree in STEM, knew how to write code, looking for a career in the tech industry -- so I started working toward it.
I began with taking the top-rated Coursera track in data science and reading all I could about data science.
At the time, it felt like data science was an ill-defined concept that included everything from web-scraping and exploratory data analysis to advanced machine learning models.
I remember reading an article at one point that there were three "stages" to data science:
1. Data extraction, cleanup, and preparation (what the industry now calls Data Engineering)
2. Data analysis and modelling
3. Presentation of the results

I really latched onto this model of data science and used it to guide my own discussions of the work.
In interviews, when asked what I wanted to work on, I would explain this model and confidently state that I was most interested in stages 1 and 3.
In the spring of 2015, I participated in a 6 week data science boot camp program called [the Data Incubator](https://www.thedataincubator.com/) designed specifically for STEM PhDs to transition to careers in data science.
The program was great, it gave me my first real experience working on AWS, an introduction to MapReduce, and opportunity to learn alongside a diverse group of people with a shared interest.

Ultimately, I got my first job in industry via a short-term contract with a series A startup in Berkeley, California.
As so often happens in these situations, the job ended up being something completely different than I signed up for.
They hired me as a "Data Architect" and after less than a month, the CTO decided I should be called a "Systems Engineer" when printing business cards for the team.
Over the course of just a few months, I learned a lot and made a big impact with a small team of 5 engineers.
We built our own MapReduce framework using Docker Swarm with the orchestrator written using Docker's Python API (how this came to be is a story for another day).
Then we refactored the existing monolithic LiDAR registration and alignment code into a series of three MapReduce steps.
Throughout, I learned a lot about working on a shared codebase, merge requests, the value of unit tests, and wrote more lines of code in those three months than I did in my whole doctorate. 

Once that contract ended, I got a job in the big 'R' research group at [HERE Technologies](https://www.here.com/).
I started that role doing platform engineering work building tools to support the projects other members of the team were leading.
This included some exploratory work testing various databases' geospatial query capabilities and writing a webapp that acted as a frontend for an internal data acquisition API.
This webapp was a project I loved building and continued to support for a couple years after the main work on it was done.
I built a Flask application that, given the data constraints someone wanted, would query the API for that data, download it onto S3, and then run an EMR pipeline of common data cleaning and preparation methods that were used across the team.
Alongside this, I participated in algorithm development using GPS probe data for map maintenance and real-time traffic prediction.
One project, using this data to predict road closures from probe data, resulted in a [patent application](https://patents.justia.com/patent/20200105134) and was published in a special issue of [ACM Transaction on Spatial Algorithms and Systems on Urban Mobility](https://doi.org/10.1145/3325912).
Other work included development of a change detection pipeline using sensor data from vehicles to detect missing or changed map features in HERE's high definition map for autonomous vehicles.
After a three years on the research team, I transferred to a team that brought this change detection pipeline into production.
Bringing us to today, where I am on that same team, which is continuing to work on the change detection problem, and we have a new project building a data service that analyzes and caches streaming sensor data, sending bundles of co-spatial data to the change detection service. 
