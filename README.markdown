# Problem Overview

You are a lab tech in a pretend lab and have been tasked with making a tool to determine the number of target sequences inside a reference genome.  When looking for a genetic match you will need to search for both the original target sequence and its reverse complement, see google for details of doing a reverse complement of a DNA sequence. You will use Django to build a web form which will take in target and reference sequences and return the number of times the reference sequence can be found in the target.

You are welcome to use whatever resources and tools you like.

# Examples

Reference genome GATATC and Target sequence ATC will have 2 matches: 1 at the 3rd index on the reference genome and 1 at the 2nd index going in the reverse direction.

Reference genome ATCCT and Target sequence ATC will have 1 match at the 0th index.

Reference genome CATATGGGCAT and Target sequence CAT will have 3 matches: 2 are at the 0th and 8th indices on the reference genome and 1 is at the 5th index going in the reverse direction.

Reference genome ACTACTACT and Target sequence ACTACT will have 2 matches at the 0th, and 3rd indices.


# Details

- Going to the url /genome_form should return a form with two required inputs "Reference Genome" and "Target Sequence".  Remember the strings for the reference genome can be incredibly long (5 million characters or more). Target sequences can be assumed to be much shorter, approximately 50 characters or less.
- To find a match you will need to take the target sequence and calculate its reverse complement.  Then take both the target and its reverse complement and search for each in the reference.
- A successful post to the same url should return the form filled out along with the number of matches and locations within the reference.
- For long reference genomes this could take a long time so create a model for saving the reference genome and target sequence as well as the locations of any matches.  If a model with a matching reference and target sequence exists skip the calculation and just return the cached information.
- Both fields are required and should validate that they are properly formatted DNA sequences meaning strings only containing C, A, T, and G. If an invalid form is posted then the user should be given clear error messages returned after the POST.
- This should be treated like a production website with all relevant code tested and commented.
- If you have remaining time, build in the ability to find fuzzy matches given a maximum number of mismatches. E.g. providing 0 as input will give only exact matches, providing 3 will find matches where up to 3 characters do not match, etc.


# Deliverables

Please create a zip file from your project folder with  all relevant code, setup files, and a ReadMe.  An example ReadMe as been attached please use it as a template for creating yours and fill out all of the sections.

# Scoring

Your work will primarily be evaluated based on the test quality, code readability, and the clarity of information in the ReadMe.  If you have any questions about the format or become stuck please contact me directly at mikela@pivotbio.com


```markdown
# Quickstart Instructions

## Installation

Include here all instructions for setting up your application including installing system requirements for your prefered OS as well as language specific packages.  

## Running the server

Include instructions here required to to start and stop the development server.

## Running tests

Include instructions here for how to run tests.

# Explanation of methods

In this section please explain the method or methods you have used here including both why and how they work in general terms.  Also include an estimate of the time complexity required to determine the alterations required for an original genome of length m and desired sequence of length n.

# TODO

Explain any problems that you encountered and possible solutions you would implement if you had time.  This is also a good place to describe any UI and operational improvement you might want to make in the future.


```
