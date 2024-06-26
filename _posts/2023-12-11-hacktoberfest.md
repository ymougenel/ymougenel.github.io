---
layout: post 
title: Hacktoberfest, SpringBoot & Jenkins contributions
excerpt_separator: <!--more-->
tags: [Open-Source, java, events]
---
I joined the 2023 Hacktoberfest event, and managed to end up with 3 main contributions:
* [A bug fix](https://github.com/jenkinsci/slack-plugin/pull/929) on the **Jenkins Slack-plugin**
* [A small enhancement](https://github.com/spring-io/initializr/pull/1492) on the **spring-boot initializr project**
* [A translation fix](https://github.com/jenkinsci/text-finder-plugin/pull/206) for the **"text-finder" Jenkins plugin**

<img src="../assets/jenkins.png" width="15%">
<img src="../assets/slack.jpg" width="21%">
<img src="../assets/springboot.png" width="21%">
<br>
It has been some time since I last took part in the Hacktoberfest open-source events.  
This year, I came in with a handful of goals and minimal time to spare, and here's how it all played out:
<!--more-->

# The event
[Hacktoberfest](https://hacktoberfest.com/) happens every year in October, it is a free event which encourages open-source contribution.  
I took part in the event in 2017 and wanted to give it another shot this year.

# Goals for this year
As I started a new job on September, I had limited time for this October challenge. Therefore I went with a straight forward strategy: 
* Finding existing OS issues that do not require a huge onboarding. 
* Focusing on Java & Python, which are my main programming languages.


I did some preparation for the event by searching open-sourced projects on Github & Gitlab (both platforms provide Hacktoberfest Topics).


Here are the final contributions:

# Jenkins __Slack-Plugin__: a pipeline status error
On my current job we use the Slack/Jenkins plugin, which send pipeline status and messages on Slack.  


When noticing [this existing issue](https://github.com/jenkinsci/slack-plugin/issues/818) regarding a pipeline error not setting the right build status, 
I immediately got inspired: I had already worked on Jenkins plugins before, and was vaguely familiar with the pipeline status behaviour:

1. Reproduce the bug: I set up a new Jenkins dockerized environment, re-used an old Slack account, built and deployed the plugin on it.
2. Isolate the concerned code base . Jenkins' plugins usually works through steps. The faulty steps had to identified and fixed.
3. Testing: I manually tested few scenarios, and added **unit tests** to avoid any further regressions.

| [Github MR](https://github.com/jenkinsci/slack-plugin/pull/929) &ensp;&ensp;&ensp; | **status:** accepted & closed &ensp;&ensp;&ensp; | **time spent:** ~4 hours |

# Spring-io initializr: Synchronizing the zip file name with the artefact ID
As I participated in an open-source coding night at my company [Takima](https://www.takima.fr/), I encountered minor issues related to the Spring Framework.  

[This one issue](https://github.com/spring-io/start.spring.io/issues/163) in particular caught my eye: the zip name generated by Spring Initializr sometimes didn't match the project artefact ID. 

After compiling a huge codebase (both start.spring.io and Initializr), fixing it implied a small refactoring in order to synchronize the naming process for both the artefactId and the zip file.

| [Github MR](https://github.com/spring-io/initializr/pull/1492) &ensp;&ensp;&ensp; | **status:** accepted & closed &ensp;&ensp;&ensp; | **time spent:** ~2 hours |

# Text-finder Jenkins plugin, a translation contribution that became a fix
Back in the old days, I started my open-source journey by doing some Jenkins plugin French translations.  
Due to the lack of time, I decided that my last contribution would be a translation; and found an interesting [Jenkins plugin](https://github.com/jenkinsci/text-finder-plugin) already available in English and Japanese, but not in French.

However, during the translation into French, I noticed that the plugin's folder structure for translations was incorrect, resulting in most of the Japanese translations being ignored.

I reorganized the structure to ensure that all translations were properly incorporated.  
It ended up taking much more time than anticipated (finding the correct structure and testing for all languages), but it ultimately proved successful.

| [Github MR](https://github.com/jenkinsci/text-finder-plugin/pull/206) &ensp;&ensp;&ensp; | **status:** accepted & closed &ensp;&ensp;&ensp; | **time spent:** ~3 hours |

# Global summary

| ✅ 3 contributions accepted&nbsp;                                 |   ❌ Overlaped in November |
| ✅ 3 distinct projects  &ensp;&ensp;&ensp;                        |   ❌ Only Java projects    |
| ✅ Various types of pull requests.                                |   |

<br>
