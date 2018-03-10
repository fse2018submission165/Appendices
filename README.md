# Data release for ecosystem survey

## About the survey

This was a survey of 2321 software developers conducted in August and September 2016.
Details, motivation, and explanation of methodology are in the file "paper-and-appendix.pdf"

The survey was quite long, and only about half of the people who started it finished
it.  We include partial results here, since we put the most interesting questions first,
and wanted to include those answers.

There are several questions in the middle of the survey (see Key.xslx for details)
that were only included for some participants -- we did not ask about "upstream practices"
if respondent answered that their package was not used by others.  Answers that people
simply skipped over are marked "Skipped"; answers that were never posed, or on pages
past the end of a partially completed survey, are marked as "NA".

## Preprocessing

We used Qualtrics to administer the survey. Rather than provide the raw data downloaded
from Qualtrics, we preprocess it to convert numeric codes for multiple choice selections
into text, since the numeric codes in some cases would sort answers in counterintuitive
ways.

Motivation values (motive.int, motive.sta, motive.uv) are calculated by weighing specific
motivation question answers from:

    Jeffrey A. Roberts, Il-Horn Hann, and Sandra A. Slaughter. 2006. Understanding the Motivations,
    Participation, and Performance of Open Source Software Developers: A Longitudinal Study of the
    Apache Projects. Manage. Sci. 52, 7 (2006), 984–999. http://dx.doi.org/10.1287/mnsc.1060.0554


## Anonymization

Because the survey included several demographic questions and asked about
smallish software ecosystems, it could be possible to individually identify some
people who took the survey.  To protect their anonymity, we have made the
following modifications to the data, merging options and omitting questions
so that unique and identifiable combinations of answers do not occur.

* Ecosystem: changed to "other" if fewer than 15 people completed the survey
* my.eco.role: We have merged the "founder" and "lead+" roles into a single category, "central"
* my.eco.years, oss.experience, dev.experience: We have merged these into two categories: "<5 yrs", "5+ years"
* my.package.name: We omit the name of the package the user chose to answer questions about
* age and gender: We have omitted these; most respondents were young and male, so other responses become an identification risk

We also exclude the free text fields, many answers gave identifying information
or wrote in a distinctive style.

If you need the omitted data for research, please contact us and we can discuss
mutual interests and the process for applying for IRB* approval.

*IRB = Institutional Review Board, the ethics committee that oversees research to
protect the privacy and safety of participants.
