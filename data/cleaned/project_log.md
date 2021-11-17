 -  Cloning my personal GH repository on CyVerse Cloud shell
          
             -  `git clone https://github.com/Mychael23/miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR.git`
               
        -  Using iCommands put copy of your cloned repo in the Data Store via CyVerse Cloud shell 
                  
               -  `iinit # setup iCommands`
               -  `iput -rP # put copy of your cloned repo in the Data Store`
               -  `iput -rP miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR .`
           
Push notebooks back to my GH project repository 
        - Generate a GH access token                                                                    - "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"
        - Configure git on the CyVerse webshell instance by installing Github CLI via
            - `conda install gh --channel conda-forge`
                             
            - `gh auth login`
            - paste GH token after following prompts for `gh auth login`
            
         - Syncronize changes on Data Store to web shell instance
           - `irsync -rv i:/iplant/home/mnaddo/miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR miRNA-expression-in-multiple-rainbow-trout-tissues-during-MR `
           -  git commit -am "update project_log.md"
        - Push back to Github 
