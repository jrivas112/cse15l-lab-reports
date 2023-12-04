# Lab Report 4 - Vim (Week 7)
### Steps Taken
1. I logged into the server by doing ```ssh cs15lfa23sj@ieng6.ucsd.edu``` then ```<enter>``` then I typed my password <br><img src="images/loginintoserver.png" width=400>
2. I typed ```git clone git@github.com:jrivas112/lab7.git``` then ```<enter>```.<br><img src="images/gitclone.png" width=400>
3. Then I typed ```cd la``` then ```<tab>``` to auto-complete "lab7" then ```cd lab7``` to go into the directory then ```<enter>```. <br> <img src="images/cdlab7.png" width=400>
4. Then I typed ```bash te``` then ```<tab>``` to auto-complete "test.sh" then ```bash test.sh``` then  ```<enter>```, this showed the test's failure.<br><img src="images/Screen Shot 2023-11-19 at 8.38.19 PM.png" width=400>
5. Then I typed ```vim ListEx``` then ```<tab>``` to auto-complete  "ListExamples.java" then ```vim ListExamples.java```then ```<enter>``` to fix the code.<br><img src="images/vim3.png" width=400>
6. Then I used ":" in vim to use the vim command ```":44, 44 s/index1/index2/g"``` in order to change index1 to index2 which fixed the problem.<br><img src="images/vim1.png" width=400>
7. Then I used the command ``` :wq!``` in vim to save and exit<br><img src="images/vim2.png" width=400>
8. Then I went ```<up><up>``` back to the command ```bash test.sh``` then ```<enter>``` in order to run the test again. The test was now successful<br><img src="images/Screen Shot 2023-11-19 at 8.50.50 PM.png" width=400 >
9. Then I did ```git commit``` then ```<enter>``` to save my work<br><img src="images/Screen Shot 2023-11-19 at 9.24.46 PM.png" width=400>
10. Then I typed ```git push``` then ```<enter>``` to push it to the repo<br><img src="images/Screen Shot 2023-11-19 at 9.25.14 PM.png" width=400>
