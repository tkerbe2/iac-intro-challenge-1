![tkdev_space_200](https://github.com/user-attachments/assets/31af05be-97b5-4d4e-82ef-4f23203eb7ac)

<br>

# 🛠️ Fix and deploy Terraform to AWS - Challenge 1

Welcome to your first challenge! In this challenge you will put yourself in the role of a DevOps professional who has been given this code from a colleague. Your colleague is trying to deploy a simple EC2 instance to AWS that they can SSH into and run some tests.
Your colleague has given you this code and mentioned that they're not very experienced with Terraform and need some help. I've left parts of this code blank and expect you to use your current knowledge, existing course material, and resources such as the Terraform Registry to make some simple fixes and deploy it. 
When you're finished or you have gotten stuck - the "fixed" branch of this repo has the correct working code. 

## High-Level Steps

- Log into your personal GitHub.
- Fork this repo to your own personal GitHub.
- Clone the repo to your local machine.
- Open the it with Visual Studio Code.
- Look for comments marked by a #.
- Make the necessary fixes to the code.
- Commit your code changes.
- Open [HCP Terraform](https://app.terraform.io/app) and create a new workspace under workspaces.
- Set variables.
- Perform a plan and apply.
- Deploy your code.
- Verify resources in the AWS Console.
- *(Optional) Add an SSH allow policy to the EC2 instance security group.*
- *(Optional) Log into the EC2 instance.*


# 🏁 When ready start challenge walk-through here

<br>

## GitHub and Visual Studio Code Steps

### 1. Log into your personal [GitHub](https://github.com/) and fork this repo.

<img width="1093" height="60" alt="image" src="https://github.com/user-attachments/assets/06e231be-c11c-4f6d-a35f-2b5fc638311f" />

***

<br>

### 2. On your local machine open the code.
You can access and modify this code how you want. Ultimately all that matters is the changes get pushed to your GitHub repo.

- You can open this code remotely in Visual Studio Code (which is what I am doing in this walk-through).
- In Visual Studio Code you will want the Remote Repositories extension.

<img width="350" height="78" alt="image" src="https://github.com/user-attachments/assets/f7712344-6ed0-4fb8-a828-71814907931a" />

- On the bottom left click on the >< button to open the remote repositories

<br>

<img width="403" height="126" alt="image" src="https://github.com/user-attachments/assets/81daf9db-48fc-4734-9757-862f67cfed93" />

<br>

<img width="633" height="203" alt="image" src="https://github.com/user-attachments/assets/cd75d0f7-96c7-4efd-90c7-593055ed8521" />

<br>

<img width="629" height="161" alt="image" src="https://github.com/user-attachments/assets/92c0609f-a41d-47b8-9771-68f1a80c3968" />

- Trust the workspace so your extensions work.

<br>

<img width="442" height="378" alt="image" src="https://github.com/user-attachments/assets/ebc64217-010a-45ce-97f7-1525b4df37c2" />


### OR

- You can clone the repo to your local machine and push the changes remotely.
- [Follow these steps on Microsoft Learn](https://learn.microsoft.com/en-us/azure/developer/javascript/how-to/with-visual-studio-code/clone-github-repository?tabs=activity-bar)

<br>

***

<br>

### 3. 🛑 Fix the code!
- Look for commented code and start finding solutions. This is where you actually will be spending a majority of your time in this challenge. Use your resources and other lab material!
- Remeber you're role playing as a DevOps Engineer and your colleague has given you some unfinished code. Read their comments and try to fix it so that you can deploy it using HCP Terraform.
- Once you're ready and believe you've fixed the code you can proceed. 

***

<br>

### 4. Commit and Push your changes.

<img width="404" height="171" alt="image" src="https://github.com/user-attachments/assets/5ba69cb4-d926-44d7-930a-12f8542ef754" />

***

<br>

## HCP Terraform Steps
When you're finished modifying your code and think you have the right solution, you can test it with HCP Terraform. These next steps will walk your through this process. 

***

<br>

### 1. Log into the [HCP Terraform](https://app.terraform.io/app) web console.

<img width="279" height="252" alt="image" src="https://github.com/user-attachments/assets/c9348106-8030-4268-8fbe-6edceb16096e" />

<br>

<img width="214" height="140" alt="image" src="https://github.com/user-attachments/assets/601316c3-de52-48da-a196-08cc9c422808" />

***

<br>

### 2. Select a project or use the default.

<img width="601" height="314" alt="image" src="https://github.com/user-attachments/assets/389c3f1b-2efa-43ba-b274-b62c7901fe0e" />

***

<br>

### 3. Select Version Control Workflow.

<img width="1074" height="386" alt="image" src="https://github.com/user-attachments/assets/6c7bfb74-1fbd-4473-8e7b-b4424b2388e0" />

***

<br>

### 4. Click on GitHub and choose a repo. (You may have to log into and authenticate to GitHub first to allow this)

<img width="736" height="520" alt="image" src="https://github.com/user-attachments/assets/d02583ef-8186-4276-a9e4-2d8034177d07" />

***

<br>

### 5. Give it a name and click create.

<img width="101" height="54" alt="image" src="https://github.com/user-attachments/assets/22783e84-9b9b-490c-a007-a1272b5f6f37" />

***

<br>

### 6. Go to the new workspace overview and click on the Configure variables button. Alternatively you can just click on variables.

<img width="652" height="138" alt="image" src="https://github.com/user-attachments/assets/4271d3e7-ff78-419d-a2a3-40900270a819" />

<br>

<img width="276" height="232" alt="image" src="https://github.com/user-attachments/assets/1519f23f-1a43-4511-8e4d-997598d11270" />

***

<br>

### 7. Create two new workspace env variables for AWS.
We learned how to create and obtain these in the following course section:
[Setup a new AWS account - Guided Lab](https://github.com/tkerbe2/tkdev-aws-account-setup)

<img width="607" height="629" alt="image" src="https://github.com/user-attachments/assets/e030a27d-1967-4829-8f9d-f7dd7a54c865" />

<img width="1146" height="280" alt="image" src="https://github.com/user-attachments/assets/5c8071a6-6410-4c5a-b691-d571ba07c6e0" />

***

<br>

### 8. Perform a plan and apply.

- Go to Runs on the left navigation pane.

<img width="268" height="300" alt="image" src="https://github.com/user-attachments/assets/a3a490ae-1b0b-4235-91ea-ae0d49f44cb5" />

- On the right side click new run and click plan and apply.

<img width="601" height="345" alt="image" src="https://github.com/user-attachments/assets/0224b5c1-7a2d-4972-95d9-5f762e6ba28b" />

***

<br>

### 9. Plan results.

- If your plan errors you need to continue fixing your code.
<img width="1119" height="614" alt="image" src="https://github.com/user-attachments/assets/4e59cd53-e1d4-461f-a1ed-2c4d5114639c" />

- If your plan is successful you can go ahead and scroll down and hit confirm to deploy the infrastructure.
<img width="1125" height="568" alt="image" src="https://github.com/user-attachments/assets/8a1b3109-ffd8-4632-9455-7b6ebae5122f" />

***

<br>

### 10. Apply your plan.

- Scroll down to your successful plan and click confirm & apply.

<img width="833" height="237" alt="image" src="https://github.com/user-attachments/assets/f0894f15-610d-42ee-b0ca-3f6c088bc0d9" />

- ⚠️ This will actually create the resources in AWS.

***

<br>

## 🔑 Testing and Solution
You will want to log into the AWS web console and look for your resources in VPC and EC2 services.

If you're having any issues at all and want to see the solution or think you're ready to grade yourself proceed to the solution page:
[Challenge 1 Solution](https://github.com/tkerbe2/tkdev-aws-terraform-challenge-1/blob/fixed/README.md)
