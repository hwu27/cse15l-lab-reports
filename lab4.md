# Lab 4 Report
**Huaming Wu**
**A17526592**

Note: 
-An arrow indicates that the actions are done together

4 Log into ieng6

  I start off with copying my ssh details from the note app that I have on my desktop. I use Alt Tab to return to the terminal.
  
  `<Left-Click> <Left-Click> <Ctrl-C> <Alt->Tab>`
  
  In the actual terminal:
  I paste the ssh details and press enter in order to sign in. Since I already have a SSH key set up, I do not need to manually sign in.
  
  `<Ctrl-V> <enter>`

  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/8828be34-02f1-4569-9492-c4927adfaadf)

5 Git clone
    
  I copy the HTTPS link from GitHub. I click the Google Chrome icon where I have https://github.com/hwu27/lab7 open.
  Then, I click code -> Copy to Clipboard in the HTTPS section. This will allow me to paste the url and git clone. 
  I also Alt Tab in order to switch back to the terminal.
  
  `<Left-Click>` 
  `<Left-Click> <Left-Click>` (Click Code) `<Ctrl-C> <Alt->Tab>`
  git `<space>` clone `<space> <Ctrl-V> <enter>`

  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/2da682f3-5022-409c-ab87-ca2be3c2b8f7)

6 Running tests

  I am going into the cloned repository with cd and then using tab to autocomplete possible files to cd or bash to shorten my time. I use 
  bash to execute the .sh file that compiles and runs the code.
  
  cd `<space>` l `<Tab> <enter>`
  bash `<space>` t `<Tab> <enter>`
 
  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/9130ad5f-a1b8-422a-b5b0-bc26f5dfa349)

7 Editing
  
  I use vim and tab to find the file I need to edit and then enter the editor. I use / in order to search for the wordd change.
  I find that I only need to enter cha in order to find it. From there, I just used j l l as a way to move my way down and to the right.
  Lastly, I clicked r to replace 1 with 2 in index1. I then used :wq to save my work and exit.
  
  vim `<space> L <Tab>` . `<Tab>`
  /cha `<Enter>` j l l r 2
  :wq <Enter>
    
  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/3a8ab014-212e-4268-94fe-ccfb430df6d4)  

8 Check tests
  
  I used my up arrow keys twice to reuse the bash command to run the tests.
  
  `<up> <up> <Enter>`
    
  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/992c4f2b-fe65-46c4-a120-e960a94bf778)
      
9 Commit and Push

  I first use git commit -m to commit the changes to be pushed. I used -m so that I did not have to enter the vim editor. I added an update message and then
  commited the file I edited. I also used tab to autocomplete to ListExamples.java.
  
  git <space> commit <space> -m "update" L `<Tab>` . j `<Tab>`
  
  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/3017134d-085b-4d1f-9030-0eec7b535579)
  
  Here I had to go back to github using Alt-Tab and then I had to click code -> ssh -> copy to clipboard. I then Alt-Tabbed back to terminal and 
  pasted it. I clicked enter and it pushed the updated file into GitHub.
  
  git `<space> <Alt-Tab> <Left-Click> <Left-Click> <Ctrl-C> <Alt->Tab> <Ctrl-V> <Enter>`

  ![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/51708bff-7169-4d00-96cb-14e7886020ff)

