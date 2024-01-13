**Explain version control**
- Version control is also known as source control. It is the process of monitoring and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. Version control systems assist software teams in working faster and smarter as development environments evolve.
 
- Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.
 
- Version control helps teams solve these kinds of problems, tracking every individual change by each contributor and helping prevent concurrent work from conflicting. Changes made in one area of the software may be incompatible with those made by another developer working at the same time. This problem should be discovered and solved in an orderly manner without blocking the work of the rest of the team. Further, in all software development, any change can introduce new bugs on its own and new software can't be trusted until it's tested. So testing and development proceed together until a new version is ready.
 
- Good version control software supports a developer's preferred workflow without imposing one particular way of working. Ideally, it should also work on any platform rather than dictating which operating system or tool chain developers must use. Great version control systems facilitate a smooth and continuous flow of changes to the code rather than the frustrating and clumsy mechanism of file locking - giving the green light to one developer at the expense of blocking the progress of others.
 
 
 
**Explain difference between git  and github**
 
- Git is a version control system that allows developers to track changes in their code while GitHub is a web-based hosting service for git repositories. In simple terms, you can use git without Github, but you cannot use GitHub without Git.
 
- Git is a free, high-quality distributed version control system suitable for tracking modifications in source code in software development. It was originally created as an open-source system for coordinating tasks among programmers, but today it is widely used to track changes in any set of files. The key objectives of Git are as follows:
 
- Speed and efficiency
- Data integrity
- Support for distributed and non-linear workflows
 
- While Github is a web-based Git repository. This hosting service has cloud-based storage. GitHub offers all distributed version control and source code management functionality of Git while adding its own features. It makes it easier to collaborate using Git.
 
- Additionally, GitHub repositories are open to the public. Developers worldwide can interact and contribute to one another’s code, modify or improve it, making GitHub a networking site for web professionals. The process of interaction and contribution is also called social coding
 
 
**List 3 Github alternatives**
- Bitbucket
- Assembla
- Mercurial
 
 
 
**Explain difference between `git fetch` and `git pull`**
- `git fetch`, Fetches changes from a remote repository to your local repository but does not automatically merge or modify your working directory. It fetches updates for remote tracking branches in your local repository. It also downloads new branches, updates existing ones, and brings down new commits. It does not modify your working directory or merge the changes into your current branch.
 
- While `git pull`, fetches changes from a remote repository and automatically merges them into the current branch or the branch specified in the command. `git pull` is a combination of `git fetch` and `git merge`. It fetches changes and then automatically merges them into the current branch. It is a convenient way to update your local working directory with the latest changes from the remote repository.
 
 
 
 
**Explain in simple terms, `git rebase` and the command for it**
- `git rebase` is a Git command used to modify the commit history of a Git repository. It allows you to integrate changes from one branch into another by moving or combining a sequence of commits to a new base commit. The primary use case for `git rebase` is to maintain a clean and linear commit history.
 
- `git rebase main` takes commit from the other branch and replays that on top of the latest changes in the main This process to achieve this are below:
 
1. Create a new branch  `git checkout -b new_branch_name`
2. Make series of commits to this branch (`git commit -m “commit messages”`)
3. Update the main branch (`git checkout main `) - to open the main branch, then (`git pull origin main`) - to pull from remote repository
4. Rebase the new branch (`git rebase main`)
5. Resolve conflicts (`git status`) - to view conflicted files (git add conflicted_files) - to add conflicted files
6. The 5 step is repeated with `git rebase --continue` until all conflicted files are resolved
7. Push changes with `git push origin new_branch`
 
 
**Explain in simple terms git cherry-pick and the command for it**
- git cherry-pick is a Git command that allows you to apply a specific commit from one branch onto another branch. This is useful when you want to pick and choose specific changes or fixes from one branch and apply them to another.
 
- The process to achieve this are below:
1. Identify the commit you intend to pick using `git log ` or github (this is to obtain the hash of the commit)
2. Switfch to the branch where you want to apply the commit to by using `git checkout target_branch`
3. Apply the commit to the branch using `git cherry-pick commit_hash`
4. Resolve conflicts using `git status` to check conflicted files and `git stage conflicted_files` to add the conflicted files  
5. Repeat the `git cherry-pick --continue`  