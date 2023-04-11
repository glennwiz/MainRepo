# Tutorial: Using Git Submodules

Let's start by defining what a submodule is. A Git submodule is essentially a Git repository embedded within another Git repository. This means that you can have a separate Git repository for a specific module or component of your project, and then include it as a submodule within your main project repository. This can be useful when you want to manage multiple repositories as part of a larger project.

For this tutorial, we will create four repositories, each with a README file, and then use one of the repositories as a submodule in another repository. Here are the steps to follow:

1. Create a new repository on GitHub. Let's call this repository "MainRepo".
2. Clone the MainRepo repository to your local machine using the following command:

        git clone https://github.com/your-username/MainRepo.git

3. Navigate to the MainRepo directory on your local machine.
4. Create a new file called "README.md" in the MainRepo directory.
5. Add some content to the README file, and then commit the changes:

        git add README.md
        git commit -m "Added README file"
        git push origin main


6. Repeat steps 1-5 to create three more repositories with their own README files. Let's call these repositories "Repo1", "Repo2", and "Repo3".
7. Navigate to the MainRepo directory on your local machine, and then use the following command to add Repo1 as a submodule:

        git submodule add https://github.com/your-username/Repo1.git
           - This command will clone the Repo1 repository and add it as a submodule in the MainRepo directory.

8. Use the following command to check the status of the submodule:
        
        git submodule status
           - You should see something like this:
           - e9cb9ca8e1b2d1f3116c5f6bba7786c5c2b79a20 Repo1 (heads/main)
           - This indicates that the Repo1 repository is now a submodule in the MainRepo directory.

9. Navigate to the Repo1 directory in the MainRepo directory:

       cd Repo1 


10. Create a new file called "submodule-file.md" in the Repo1 directory.
11. Add some content to the submodule file, and then commit the changes:

        git add submodule-file.md
        git commit -m "Added submodule file"
        git push origin main

12. Navigate back to the MainRepo directory:

        cd ..

13. Commit the changes to the MainRepo repository:

        git add .
        git commit -m "Added submodule"
        git push origin main
        
14. If you want to update the submodule to the latest commit, use the following command:

        git submodule update --remote
           - This will update the submodule to the latest commit in the Repo1 repository.


        
