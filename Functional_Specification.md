# Overview

Tardigrade is a web-based application for managing enrollments, in the sense of belonging to and attending an institution (school, work, sports, training classes, etc.).
It is designed to be general enough to handle any applicable use case, though the primary expectation is that it would be used to handle delegated scholastic enrollments -- that is,
the dependents of the application's users. Some questions that it is designed to answer:

  * how many days of school does Johnny have left this year?
  * what do my three childrens' school and activity schedules look like this week?
  * who is picking up Tommy from school today?
  * how many times has Cece been in my son's class over the years?
  * my daughter's birthday is coming up; what are the email addresses of the parents of all the children in her class?
  * how are my son's grades this term?

# Stakeholders

Lead Developer: Mark Tyrrell (@tyrrminal)

# User Roles

* Parents/Guardians - the primary intended users of the application, who will interact with it to create family groups, invite secondary users, input scheduling, class, and grade data, etc.

* Enrollees - the students/workers/etc. In some cases, they will manage their own data as above, but more often they will be restricted users who can only view selected information, e.g., class schedules

* Secondary users - invited by family group owners, these users may manage data, but more often will just have access to see, e.g. when they have transportation responsibilities

* Contacts - individuals who have no read or write access to the system, but have relational user records, for instance classmates or their parents

# Use Cases

### Pam

*Calendar schedules; transportation alerts*

Pam is a mother of two, Cece (12) and Karen (8), living in the Scranton, PA. Cece attends Scranton Middle School 
from 7:25 until 1:35 and Karen goes to Scranton Upper Elementary from 8:15 until 2:25 each weekday, except for 
the multitude of holidays, professional development days, and half days scattered throughout the September-June 
school year. 

Pam and her husband Jim both work full-time, with offset schedules so that Pam can do morning drop-offs 
and Jim picks the girls up at the end of the day. However, Jim's company requires him to work late on the 
second Friday of each month for team-building exercises, and on those days, Jim's mother Marie does the 
pickups. Furthermore, midway through the Fall, Karen joined an afterschool STEAM group which meets on Fridays,
delaying her departure from school until 3:45.

Pam tries to keep track of this schedule in a shared calendar so that she, Jim, and Marie can all see who is
responsible for pickups on which days, but the recurrances and exceptions make editing it difficult. By Christmas, Karen
had been forgotten at school twice, and Marie now phones Pam twice each week to confirm the schedules, stealing precious
minutes of productivity away. What she needs is a system that considers recurring schedules with exceptions and can
audit the data to ensure that no one's being missed and send notifications and reminders to Marie and Jim.

### Ryan

*Classmate contact info*

Ryan is a single-dad of Gabe (11). Gabe is in 6th grade and makes friends easily -- but unfortunately he's a bit 
absent-minded and forgets  minor details like their birthdays, favorite foods, and... names. Gabe's birthday is 
coming up and Ryan needs to send out invitations to his classmates for the party. They can't invite everyone, but
definitely should invite Gabe's current classmates who have been in the same class together at least 3 years, out of
the seven that Gabe has been attending public schools. Ryan needs a way to collate this data and get the email addresses
of those children's parents so he can deliver the invitations.

### Michael

*Dynamic context-aware day counting; automated API access*

Michael's daughter Kelly is obsessed with time, timers, and especially countdowns. Every morning, she requires Michael
to tell her exactly how many school days she has left until summer vacation. This wasn't too tough at the beginning of
September, counting down from the 180 required school days, but by mid-January it's gotten difficult to count from either
end, especially given the pushbacks related to snow days. It would be great if he could set up the smart mirror in the front
hall (which already displays useful information like calendar appointments and the weather) to calculate the number and 
display it as well.

### Erin

*Grades and assignment tracking*

Erin is an 18-year-old student attending her freshman year of college. She's struggling with adapting to the difference in
expectations and class scheduling and her grades are suffering as a result. Even worse, one of her classes is at 9AM on Mondays,
but 10:30 on Wednesdays and Fridays. She can't keep track of it all so she's forgetting when her classes are, not to mention when 
her assignments are due. She needs a system she can set up one time with her class schedule and any exceptions to that schedule
(like holidays), and then see that schedule on her phone's calendar. Furthermore, she needs to be able to put her homework assignments
and projects into the system and have their due dates appear on her calendar as well. Finally, once she's got her schedule down,
she needs to be able to estimate her grades in each class so she knows how she's doing for getting caught up.

# Functional Requirements

In order to meet the needs of Pam, Ryan, Michael, and Erin, Tardigrade will need functionality in four fundamental realms,
with some overlap and coordination necessary between them:

#### Pods, Institutions, and Enrollment

A Pod is a group of family and friends who share (some) data. All information stored by Tardigrade is Pod-centric and
visible only to users belonging to that Pod. Users can be members of multiple Pods, and those who are have the ability
to copy some data between Pods to which they belong. A Pod member is assigned a single Pod Role, which dictates what
privileges that user has in the Pod.

#### Schedules and Calendars

#### Contacts and Contact Information

#### Grades and Assignements