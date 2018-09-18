# Assignment-1.2
assignment 1.2 for Acadgild Data Science with R course


1. What should the output of the following Script?

v <-- c(2,5.5,6)
t <-- c(8,3,4)
print(v%/%t)

OUTPUT: 0 1 1

2. readin multiple .xlsx files to 1 data frame
#set working directory
setwd("<loction of directory>")
  filelist <-- list.files(pattern = ''\\.xlsx") # list all the xlsx files from the directory
  allxlsxfiles.list <-- list() # create a list to populate with xlsx data
  count <-- 1
    for(file in filelist) {
      data <-- read.xlsx(file,sheetIndex=1,header=TRUE)
      allxlsxfiles[[count]] <-- dat # creat a list of rows from xls files
      count <-- count + 1
    }
   allfiles <- do.call(rbind.data.frame, allxlsx.files) # convert to dataframe.
    
    
3. reading multiple .csv files into 1 dataframe
#set working directory
setwd("<loction of directory>")
  
csvfiles <-- function(directory, ids) {
  # locate the files
  files <-- list.files(directory, full.names=T)[ids]
  
  # read the files into a list of data.frames
  data.list <-- lapply(files, read.csv)
  
  # concatenate into one big data.frame
  data.cat <-- do.call(rbind, data.list)
}
