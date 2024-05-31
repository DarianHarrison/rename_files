# rename_files
a useful function to rename files in folders

```sh
for i in $(ls); do                        # runs through the 'items' in this dir                               
  if [ -d $i ]; then                      # if this is a dir
     cd $i                                    # move into the dir       
     for fname in *.tab; do               # loop over files with tab extension
       mv -- "$fname" "${fname%.tab}.tsv"       # rename files               
       echo $fname ${fname} 
     done                                        
     cd ..
  fi                                              
done
```
