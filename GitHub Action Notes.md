- <span style="font-size:16px; color:green;">GitHub</span>:
	-Platform for open-source Projects

- <span style="font-size:16px; color:green;">actions/checkout@v4:</span>
	is used in GitHub Actions workflows. It refers to the official GitHub Action that checks out (downloads) your repository code into the workflow runner so that your CI/CD job can use it.

- <span style="font-size:16px; color:green;">actions/setup-node@v4:</span>
	is a GitHub Action that sets up Node.js in your workflow environment.

- <span style="font-size:16px; color:green;">npm ci is:</span>
	used to install Node.js dependencies exactly as specified in package-lock.json

- <span style="font-size:16px; color:green;">peaceiris/actions-gh-pages@v4:</span>
	Uses the GitHub Action that handles deployment to GitHub Pages

- github_token: <span style="font-size:16px; color:green;">${{ secrets.GITHUB_TOKEN }}:</span>
	Authenticates using a built-in secret token provided by GitHub Actions

- <span style="font-size:16px; color:green;">workflow_dispatch</span>
	is a manual trigger that allows you to run a GitHub Actions workflow manually from the GitHub web interface.

GitHub Actions uses <span style="font-size:16px; color:blue;">YAML</span> to create a GitHub Action.

<span style="font-size:16px; color:green;">YAML</span> is a serialization language like <span style="font-size:16px; color:blue;">XML</span> and <span style="font-size:16px; color:blue;">JSON</span> 

- <span style="font-size:16px; color:green;">Workflows</span>:
	--A **workflow** is a configurable automated process defined in a `.yml` file inside `.github/workflows/`. It can have one or more jobs and is triggered by events like `push`, `pull_request`, or manually with `workflow_dispatch`.
		![[Pasted image 20250725152536.png]]
- <span style="font-size:16px; color:green;">Actions</span>:
	-**Actions** are reusable pieces of code that perform tasks like checking out code,   setting up environments, or deploying. You can use public actions or create your own.
		![[Pasted image 20250725152641.png]]
- <span style="font-size:16px; color:green;">Jobs</span>:
	-A **job** is a set of steps that run in the same environment (runner). Multiple jobs can run **in parallel** unless defined otherwise.
		![[Pasted image 20250725152722.png]]
- <span style="font-size:16px; color:green;">Steps</span>:
	-**Steps** are the individual tasks inside a job. They can run shell commands or use actions.
		![[Pasted image 20250725152744.png]]

- <span style="font-size:16px; color:green;">Runs</span>:
	-A **run** is an instance of a workflow being executed. It happens whenever a trigger occurs (push, pull request, or manual run). 
	ex: if a user pushes a commit, GitHub triggers a workflow **run** based on the `.yml` configuration.
	

- <span style="font-size:16px; color:green;">Runners</span>:
	-**Runners** are servers (hosted by GitHub or self-hosted) where jobs are executed. Each job runs on a runner specified by `runs-on`.
		![[Pasted image 20250725152942.png]]
- <span style="font-size:16px; color:green;">Marketplace</span>:
	-The **GitHub Actions Marketplace** is a platform where developers can **find, share, and reuse actions** created by the GitHub community or organizations. These actions can be used directly in your workflows to save time and effort. 
	ex: To cache dependencies and speed up your builds, you can use an action from the Marketplace like:
		![[Pasted image 20250725153207.png]]