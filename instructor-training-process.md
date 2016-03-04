# Trainer Training Process

This document describes the workflow for training new instructors,
and is meant as both a guide to trainers
and as a checklist for adding support for this workflow to [AMY][amy].

## Workflow

1.  **Recruiting candidates.**
    1.  People may apply directly as individuals to become instructors
        by filling in a form on our website.
    1.  People may apply in physically co-located groups.
        We have only done this one (for training in Dec 2015),
	but it worked so well that we would like it to become routine.
	In this case,
	groups need to fit between a minimum and maximum size (e.g., 3 to 12)
	and the application must includes names and contact information for everyone who intends to take part.
	Groups must also commit to organizing and running at least one workshop within a few months of training.
    1.  We may commit to training people for partner organizations as part of their partnership agreements.
        Here,
	we negotiate dates with the partner site,
	which selects the participants subject to the same per-site size restrictions above (3-12 people per site).
1.  **Matching candidates to courses.**
    This has been done manually to date:
    the lead trainer, members of the Steering Committee, and/or the Executive Directors
    decide on dates and then invite individuals and/or groups to take part.
1.  **Running courses.**
    1.  In-person courses are run over two days,
        with all participants at one site.
    1.  Live online courses are also run over two days,
        but participants take part in small groups at a small number of sites
	(typically 3-12 per site and 2-4 sites).
    1.  Asynchronous online courses are run over several weeks.
        Participants are typically *not* co-located,
	but get together for an hour of discussion online each week.
	This format is being phased out,
	as it took more effort from trainers
	and had poorer follow-through rates than the intensive two-day versions.
1.  **Homework.**
    1.  After completing the course,
        the trainee picks one core lesson from each carpentry she wants to teach
        and submits a small change for that lesson.
    1.  Changes do *not* have to be accepted in order for the trainee to move on,
        but they do have to be properly formatted.
    1.  Changes are submitted as GitHub pull requests for Software Carpentry
        and by appending them to a Google Docs page for Data Carpentry
	(because Data Carpentry doesn't teach Git,
	and therefore doesn't want to require instructors to have to know it).
    1.  Changes to content are discouraged,
	since the lessons are now fairly stable.
    1.  New exercises are also becoming problematic,
	since we already have more than we can possibly use.
    1.  Load on lesson maintainers has become unsustainable.
1.  **Discussion sessions.**
    1.  The trainee then takes part in an hour-long group discussion of that lesson
        led by an experienced instructor.
    1.  She is expected to have gone through the lesson *before* this session
        so that she can ask lots of pointed questions during that hour.
    1.  If the discussion leader feels the trainee is unprepared,
        she may be asked to do some more work and try again.
1.  **Final demonstration lessons.**
    1.  The trainee then does a short demonstration lesson via screen sharing.
    1.  If the examiner feels that she needs to do more work,
        she will be given feedback and asked to try again.
    1.  Trainees do not have to qualify separately for different topics within one Carpentry,
        but *do* have to do a separate demonstration lesson for each Carpentry.
1.  **Welcoming to the community.**
    1.  Once the trainee has passed the demonstration lesson,
        we generate a PDF certificate for the trainee by running a command-line script in
        [the certification repository][cert-repo]
	and send it to her along with instructions for the items below.
    1.  The instructions sent to the new instructor tell her to:
        1.  join the `discuss` and `instructors` lists
	1.  fill in a form on AMY to tell us where she is, what she's comfortable teaching, etc., and
	1.  send us a short biography and photo to add to [our website][team-page].
    1.  We manually add the biography and photo to the website
        (since they almost always require reformatting).

## Resources

1.  [AMY][amy] is the web application we use to track instructors and workshops.
    Most of it is only accessible to administrators,
    but it does have a form where instructors can supply or update information about themselves.
1.  There's a web form on AMY that people can use to apply for instructor training
    (currently disabled).
1.  We keep a list of trainees in a Google Docs spreadsheet with the following fields,
    which we upate manually:
    1.  name
    1.  contact email
    1.  which training course they took part in
    1.  the name of the Software Carpentry lesson they're concentrating on (if any)
    1.  the name of the Data Carpentry lesson they're concentrating on (if any)
    1.  the URL of their Software Carpentry exercise submission (if any)
    1.  whether or not they have submitted something for Data Carpentry
    1.  the date and moderator of the discussion session they have taken part in
        *   we currently store both values in one column
	*   we do not record both a Software Carpentry and a Data Carpentry discussion session (though we should)
    1.  the date on which they passed their Software Carpentry lesson demo (if any)
	*   this date becomes the award date of the PDF certificate
        *   we do not currently record the name of the person who was their instructor, or the name of the person who did their final test
    1.  the date on which they passed their Data Carpentry lesson demo (if any)
        *   the same caveats apply
1.  Mentors offer lesson discussion sessions,
    and trainees sign up for them,
    on an Etherpad.
1.  Trainers offer checkout sessions on a second Etherpad.
    Trainees sign up for sessions on that Etherpad,
    which we also presently use for taking notes during their sessions.
1.  Discussion and checkout sessions are marked in Software Carpentry's community calendar
    (a Google calendar).

## Issues

1.  As of Jan 2016,
    the form for individuals to apply to take part in training has been disabled
    while we try to clear our backlog (and come up with a better process).
1.  We used a Google web form and a spreadsheet for group applications and sorted manually.
    We are not systematically tracking whether groups run their promised workshops or not.
1.  Negotiations with partners about instructor training sessions are tracked in a Google Docs spreadsheet.
    Schedules are drawn up manually.
1.  We have never had a way to help individual training applicants find one another to form groups.
1.  Trainees are supposed to email the head of training when they submit their lesson change.
    The head of training then updates the spreadsheet
    and mails the trainee instructions on how to sign up for a discussion session on the lesson discussion Etherpad.
1.  The head of training recruit discussion leaders by mailing the mentoring list and a few individuals
    to ask for volunteers.
    When trainees want a discussion session,
    and there isn't one scheduled for their chosen lesson(s),
    they put themselves at the top of the discussion Etherpad.
    The head of training then asks mentors to set up more discussion sessions
    and gives the mentors the email addresses of people who want one of that kind.
1.  People leading discussion sessions report back to head of training by email,
    who then updates the trainee's spreadsheet entry
    and sends them mail telling them to sign up to do a demo on the lesson demo Etherpad.
1.  Using one Etherpad both to manage sign-up for demo sessions
    and to take notes during those sessions
    is confusing.
1.  When someone completes training,
    we manually create an entry in AMY to record:
    1.  their name (selected from a list, since it will have been input when they signed up for the course)
    1.  what award they're getting (also selected from a list)
    1.  the course they took
        *   people may be registered for more than one course if they fail to complete their first attempt at training
    1.  who certified them
        *   we have not been consistent about whether this is the person(s) who ran their training course
	    or the person who oversaw their final demo
1.  We used to do a blog post welcoming new instructors every time we had new ones.
    We haven't done that in a while...

[amy]: https://github.com/swcarpentry/amy/
[cert-repo]: https://github.com/swcarpentry/certification
[team-page]: http://software-carpentry.org/team/
