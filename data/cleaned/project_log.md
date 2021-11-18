### Use case example: Building a Github to VICE Apps workflow using CyVerse. 
 **Steps**
 -  launch the Cyverse Cloud Shell in the Discovery Environment
 -  Clone my personal GH repository on CyVerse Cloud shell # input the command below in the Cloud shell
          
             -  `git clone https://github.com/Mychael23/miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR.git`
               
-  Using iCommands, put  a copy of your cloned repo in the Data Store via CyVerse Cloud shell 
                  
               -  `iinit # setup iCommands`
               -  `iput -rP # put copy of your cloned repo in the Data Store`
               -  `iput -rP miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR .
               -  
 #After Analyses have been carried out or changes have beem made on Cyverse Data Store
 
 ###  Push notebooks back to my GH project repository 

-  Configure git on the CyVerse webshell instance by installing Github CLI via
               -  `conda install gh --channel conda-forge`
               - `gh auth login`
-  Generate a GH access token
               - valid for 7 days `"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"`
               - paste GH token after following prompts for `gh auth login`
-  Syncronize changes on Data Store to web shell instance 
               -   `irsync -rv i:/iplant/home/mnaddo/miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR` 
               -  `git commit -am "e.g. update project_log.md"`
       -  `Push my Ggit Project repo back to GitHu using git push`
  
---

End of Workflow
---- 
