## 1 - Screenshots of the serverless function deployments
### **Azure**
<img width="1470" alt="Screenshot 2024-10-02 at 18 02 44" src="https://github.com/user-attachments/assets/7415e066-81c5-4fd5-9c3a-f32baf7d81b3">
<img width="1470" alt="Screenshot 2024-10-02 at 18 18 05" src="https://github.com/user-attachments/assets/4efe0054-024c-4b02-8644-4331029ed77e">

### **GCP**
<img width="1463" alt="Screenshot 2024-10-02 at 19 28 37" src="https://github.com/user-attachments/assets/f9229f52-8754-4814-b966-ec8ae8aa242f">
<img width="1470" alt="Screenshot 2024-10-02 at 19 25 58" src="https://github.com/user-attachments/assets/dced658f-7800-4c95-ae02-0195226d5f23">

## 2 - Code and configuration for the GitHub cron job / Github Action workflow

    # This is a basic workflow to help you get started with Actions
 
    name:
      First Cron Job
 
      # Controls when the workflow will run on:
      # Triggers the workflow every 5 minutes schedule:
        - cron: "*/5 * * * *"
 
          # A workflow run is made up of one or more jobs that can run sequentially or in parallel jobs:
      # This workflow contains a single job called "cron"
      cron:
        # The type of runner that the job will run on
        runs-on: ubuntu-latest
 
        # Steps represent a sequence of tasks that will be executed as part of the job steps:
          # Runs a single command using the runners shell
          - name: Run a one-line script
            run: echo Hello, world!'''

<img width="1470" alt="Screenshot 2024-10-04 at 16 54 06" src="https://github.com/user-attachments/assets/3a9f8079-3d32-44d0-9375-3f8871fc2dba">
<img width="1470" alt="Screenshot 2024-10-04 at 16 54 15" src="https://github.com/user-attachments/assets/5021fa05-ff3b-4a1e-ae89-87b4e46df3fa">

        
## 3 - Documentation of the GCP Cloud Scheduler setup
### First, define the schedule by creating a project name, selecting a region and timezone, and specifying the frequency. In this case, the string 0 1 * * 0 runs the job once a week at 1 am every Sunday morning. 
<img width="1468" alt="Screenshot 2024-10-04 at 17 12 17" src="https://github.com/user-attachments/assets/89462ebe-9981-46bf-a504-42c60c9ec51f">

### Second, configure the execution by specifying the target type (https, pub/sub, app engine http)
<img width="1470" alt="Screenshot 2024-10-04 at 17 14 06" src="https://github.com/user-attachments/assets/1b1e9f85-b5d4-4285-930f-51cca97ed103">

### Lastly, configure optional settings and your cloud scheduler is ready!
<img width="1470" alt="Screenshot 2024-10-04 at 17 21 24" src="https://github.com/user-attachments/assets/c3ce48f3-71c1-4ccd-8db9-d1b468c9afec">

## 4 - A brief reflection on the use cases, benefits, and limitations of serverless functions 
Serverless functions, or Function as a Service (FaaS), provide a scalable way to build applications without managing infrastructure. They excel in microservices, event-driven architectures, RESTful APIs, scheduled tasks, and data processing. Key benefits include cost efficiency—paying only for compute time—automatic scalability, reduced management overhead, faster deployment, and built-in redundancy. However, limitations such as cold start latency, execution time limits, the need for external state management, potential vendor lock-in, and debugging challenges must be considered. While serverless functions can enhance application development, it's crucial to balance them with other architectural patterns for optimal results.




