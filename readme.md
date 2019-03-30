Class website for Sociological Gobbledygook, a.k.a. Introduction to Quantitative and Computational Legal Reasoning, University of Iowa College of Law, spring 2019. 

This used to be just the private repository for the course website, with the original plan to be to have lessons and discussions of material hosted in other repositories.  That didn't really work, so I've opened this repository to the public and am declaring it the Official Source for all lessons and such. 

Other repositories that have touched this course: 

- the [original official repository](https://github.com/paultopia/quantitative-methods-for-lawyers) which has pre-course discussions of content, and some very preliminary drafts of lesson material. 

- a [lesson repository](https://github.com/paultopia/gobbledygook_lessons) that I created to allow students to clone the first few weeks of Jupyter notebooks.  This ultimately didn't work very well, so I just made all the Jupyter notebooks directly downloadable from the website.

- a [library repository](https://github.com/paultopia/library_gobbledygook) that I created just to store a pipfile with verified working versions of every library used in the lessons, and the basis for an ipython kernel that I use to write all the lessons.  It eventually grew to include early drafts of lessons as well, and I'll probably keep using it for that purpose down the line (so as not to pollute the history of this repository with a bunch of changes) 

## TODO: 

- [ ] Move pipfile to this repository as canonical source of truth for library versions.  
- [ ] Fix the arbitrarily assigned dates for lessons in this repository.  
- [ ] Figure out a way to tag problem sets as belonging to particular iterations of the course and hold old pests in an archives section (as there will obviously have to be new ones for each session, but the old ones are good study material.  
- [ ] Fix the painfully slow build process where each lesson gets a whole new PDF generated and uploaded on every build/deploy even if no content has changed.  (This probably involves taking a fast hash of every lesson file, shoving them into a SQLite database or some such, and checking the hash before pdf converting.  But that doesn't solve the repeated upload problem, for that I'll need to write a new upload script that is rather more selective on files. Or just make the upload process be cloning the repo from the webserver.  Which might be more sensible anyway, because then I can just grant limited ssh access to run a cloning script to multiple devices and be able to deploy from anywhere.)