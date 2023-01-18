## Contents
- <a href="#version-control">Version Control</a>
- <a href="#git-and-github">Git and GitHub</a>
- <a href="#next-steps">Next Steps</a>
# GIS 3011 - Setting up your Course Environments
This semester, we will be using a couple of resources:
1. Git and GitHub for version control and documenation
2. Google Colab for working on assingments together
3. Juptyer Notebooks and Jupyter Labs (locally installed) for the actual assignments.  

In this first lesson, we will set up our accounts, connecting GitHub to Google Colab, downloading and installing Minconda, and several Pandas libraries.

## Version Control
One of the most important things is the use of version control. I'm sure by this point, you've used this concept in your other courses. As you work through the various assignments, it will be important to not only save your Jupyter notebooks, but also to create versions of that code in your private GitHub repository. That way, if you go down the wrong path, you have a history of what you did before.  This is your friend!

<img style="padding-left:12.5%" src="https://imgs.xkcd.com/comics/documents.png" />

## Git and GitHub
First, we will download and install Git and setup a GitHub account (if you don't already have one).  Git is one avaliable version control software that you may already have experience using (which will come in super handy), while GitHub is a website that hosts <strong>repositorites</strong> of data - in our case, these descriptive files and the .ipynb Notebooks which will contain our working code.
### Basic Git and GitHub Vocabulary
Here are a few basic terms that are used often when using git and GitHub (not exhaustive).
- <strong>Repository</strong> = a location where all the files for a particular project are stored, usually abbreviated to “repo.” Each project will have its own repo, which is usually located on a server and can be accessed by a unique URL (a link to GitHub page for example).
- <strong>Commit</strong> = To commit is to write or merge the changes made in the working copy back to the repository. When you commit, you are basically taking a “snapshot” of your repository at that point in time, giving you a checkpoint to which you can reevaluate or restore your project to any previous state. The terms ‘commit’ or ‘checkin’ can also be used as nouns to describe the new revision that is created as a result of committing.- Revision / version = A revision or a version is any change in made in any form to a document(s).
- <strong>Clone</strong> = Cloning means creating a repository containing the revisions from another repository. This is equivalent to pushing or pulling into an empty (newly initialized) repository. As a noun, two repositories can be said to be clones if they are kept synchronized, and contain the same revisions.
- <strong>Pull / push</strong> = Copy revisions from one repository to another. Pull is initiated by the receiving repository, while push is initiated by the source. Fetch is sometimes used as a synonym for pull, or to mean a pull followed by an update.
- <strong>Merge</strong> = A merge or integration is an operation in which two sets of changes are applied to a file or set of files.

## Next Steps (in this order)
1. Use the document "InstallGit.md" to install Git and create a personal access token
2. Use the document "InstallPostGISAndOSGeo4W.md" to install/update PostGreSQL, PostGIS, QGIS, and GRASSGIS
3. Use the document "InstallJupyter.md" to get Anaconda and Jupyter Notebooks installed
