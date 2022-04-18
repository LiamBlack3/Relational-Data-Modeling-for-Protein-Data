# Relational-Data-Modeling-for-Protein-Data
To create an SQL build file for an extended database. To learn how to integrate more tables to a previously created database in SQLite3 to store downloaded data.


# Introduction
Often when you create a database, you will find it necessary to add extra tables to be able to enhance its use. In this lab, you will modify the SQL builder code from your previous lab (i.e., the file proteinDB build.txt) to contain two additional tables, containing the downloaded protein data from https://www.uniprot.org/ from searches for m-protein and sars. We note that these two additional tables will contain protein data which we believe to have connections to the original data from the original database.

Please note, you will not be using this command in the SQLite environment, this command is to be used at the TERMINAL (unix) prompt in your Docker container. The below command will be necessary to build the database from with a UNIX or Docker environment.
cat proteinDB2 build.txt | sqlite3 proteinDB2.sqlite3

# How to run this builder

cat proteinDB2_build.txt | sqlite3 proteinDB2.sqlite3 

# Reference
Your database is to contain the data from the following sources. This implies that this database will have four tables in total.
• From last lab, n-protein: https://www.uniprot.org/uniprot/?query=n-protein&sort= score
• From last lab, s-protein: https://www.uniprot.org/uniprot/?query=s-protein&sort= score
• New table for Sars: https://www.uniprot.org/uniprot/?query=sars&sort=score
• New table for m-protein: https://www.uniprot.org/uniprot/?query=m-protein&sort=
score
