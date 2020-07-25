---
title: Let the bots help find you a job
date: "2020-05-12T01:00:11Z"
featuredImage: './RobotReminder.png'
---

![Issues](./GHIssues.png)

<sub>Updated 2020-07-24</sub>

Ok, so now you must search for a job. I have been there. I have tried to track my applications and related material through email, spreadsheets, etc. I have never successfully followed up on jobs consistently until my last job search. On a whim, I decided to try using GitHub for this round. Surprisingly it worked well, better than I expected. Then I found one of my favorite bots.

## Stale-bot

Set me to introduce (or re-introduce) you to Stale-bot. Stale is a free bot on Github. Its traditional purpose is to mark issues as stale (as the name suggests) after a predetermined amount of time. I decided to use its functionality in a slightly different way. I am using the bot as a reminder generating bot to remind me to follow up on the jobs I have applied. Below is the configuration I used to get a reminder every seven days to follow up.

```yaml
# Number of days of inactivity before an issue becomes stale
daysUntilStale: 7
# Number of days of inactivity before a stale issue is closed
daysUntilClose: 30
# Issues with these labels will never be considered stale
exemptLabels:
  - pinned
  - No follow up needed
  - Unsure How to follow up
# Label to use when marking an issue as stale
staleLabel: Time for follow up
# Comment to post when marking an issue as stale. Set to `false` to disable
markComment: >
  It has been 7 days since the last activity on this application. Time to follow up
# Comment to post when closing a stale issue. Set to `false` to disable
closeComment: false
```

## Gigantic notes space

Within Github issues, you have a nearly unlimited space to put information. I used the description section of the issue to hold the job description. Some application sites hide the job description once you hit apply. If you have copied the job description, you can also use it when talking to the recruiter, interviewer, or when giving follow up.

I used the comment space to track any correspondence. The comments included whom I talked to, a copy of the email I sent, or the script for my voicemail. If you follow up with a company more than one time, you can reference the last follow up for context. Finally, you can track all of your interactions with a company (may be needed for unemployment).

## Other Github Perks

### Labels

I use labels to mark where I found the posting, how I applied, and if I received an interview. You can customize the labels color text and even emoji to suit your styles. Oh, and by the way, you can filter by labels as well. That is a trick I use on a near-daily basis. I sort by jobs buy if they have the `time for follow up` label and then by least recently updated (do the oldest first).

### Search 🔎

In my last job search, I applied for a lot of jobs. Many job boards had the same job listed. I had to make sure I was not double applying for any given position. When I used Github in the ways I described, I could search for keywords or job titles to see if I had already applied. The search looks through your title, description, comments, and labels to find any matches to your terms.

I also used search when I would get calls from jobs I had applied and when recruiters would cold call me. Since Github has an iOS app, I could have the job description in front of me within seconds, no matter what time they called. Once I had it in front of me, I could use the keywords for the job.

### Sort/filter issues

I created a shortcut to get to all of my issues that were marked for follow up, sorted by least recently updated first. I could jump on my computer, open the window, and tackle many jobs within a short amount of time. The sorted list helped me not miss my follow-ups by letting one fall through the crack.

## App built for exporting

When I started using this process, I was on unemployment. I knew that the State could ask for a detail of all the job-seeking activity I had accomplished on any given week. To this end, I created an OAuth GraphQL app that generates an excel file with all the issues from a given repository. It may not be the final form of your need. However, it will get you close. Current app address is <https://github-issues-to-excel.netlify.app/>. *Feel free to send in pull requests for new features.*

## Closing thoughts

Applying for a job is hard. Follow-up is key to getting a position. Let the bots help you find your next job, position, career, etc.

God Bless.
