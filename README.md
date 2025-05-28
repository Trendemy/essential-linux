# Linux Commands Practice Lab

## Objective  
Practice common Linux commands. Each exercise requires combining multiple commands such as `grep`, `awk`, `cut`, `xargs`, `find`, `rsync`, `systemctl`, etc.

## Instructions  
1. Clone the exercise repository to your local machine:  
   ```bash
   git clone [<repo-url>](https://github.com/Trendemy/essential-linux.git)
   cd essential-linux
   ```
2. Create a new branch with your name:  
   ```bash
   git checkout -b <your-name>
   ```
3. Answer the questions in the file `answers/your-name/answers.md`. For each question, include:
   - The command(s) used  
   - The output  
   - A brief explanation  

4. Commit and push your branch to the repository:  
   ```bash
   git add .
   git commit -m "lab answers from <your-name>"
   git push origin <your-name>
   ```

## Exercises  
1. Find the IP address with the most errors in `access.log`.  
2. List all usernames that do not use `/bin/bash` from `users.csv`.  
3. Use `sed` to update `config.conf` and compare the changes.  
4. Search for `timeout` errors in all `.log` files.  
5. Count the occurrences of each error type in `error.log`.  
6. Find the process consuming the most CPU.  
7. Use `rsync` to back up `.conf` files, excluding any containing `*default*`.  
8. Filter out non-duplicate lines between `access.log` and `error.log`.  
9. Search for the word `dummy` inside `archive.tar.gz`.  
10. Check and start the `nginx` service, then filter logs containing "fail".
