# DevOps Task – Write-up

## Tools and Services Used
- Node.js for building the application  
- Docker for containerizing the app  
- Jenkins for CI/CD automation  
- GitHub for version control  
- AWS EC2 (Ubuntu) for hosting  

---

## Challenges Faced and How I Solved Them

1. **Container name conflict**  
   The pipeline failed because the container name `node-app` was already in use.  
   I fixed this by adding a step in the Jenkinsfile to remove the old container before starting a new one.

2. **Error in app.js**  
   At first, the app had a syntax error in the `app.listen` function which stopped the container from running.  
   I corrected the code to:  
   ```js
   app.listen(3000, () => {
     console.log("Server running on http://localhost:3000");
   });
