# 2.1.3 Data Error Prevention, Enhancement, and Preparation for Distribution - Pete Alonzi October 22, 2018
## 2.1.3.1 Error Prevention
### 2.1.3.1.1 Valid Values (Enumeration)
* column I (semesters_worked): need to choose between words or numbers
  * for example row 31-33 are words not numbers so they are invalid (but do contain info we like)
  * sometimes the way to fix is to do it by hand - **sort the dataset on column I, discuss how to fix**
* [Enumeration](https://en.wikipedia.org/wiki/Enumeration)
  * The term is commonly used in mathematics and computer science to refer to a listing of all of the elements of a set. The precise requirements for an enumeration (for example, whether the set must be finite, or whether the list is allowed to contain repetitions) depend on the discipline of study and the context of a given problem.
  
### 2.1.3.1.2 Range Checking
* classic example is Nuclear Ghandi in the video game Civilization
  * https://knowyourmeme.com/memes/nuclear-gandhi
  * Ghandi starts the game as super peaceful, but if you do something to placate him he becomes super aggressive
  * He start with aggression = 0, so when you give him -1 it becomes 7, becuase it was 1-bit in the programming
* practice with column H - badge #
  * in this case we can just make an artificial constraint say we only want badges below 250,000
  * create a new column using a function IF(H2<250000,"VALID","INVALID")
  
### 2.1.3.1.3 Duplicate Records
* IF(COUNTIF($A$2:$A$<<lastrow>>, $A2)>1, "Duplicate", "Unique")

## 2.1.3.2 Enhancing Your Data
### 2.1.3.2.1 Splitting/Joining Columns
### 2.1.3.2.2 Joining Tables (not the database definition)
* using content from one sheet in another sheet
* it is important to not duplicate data because then you need to update it in multiple places
* excel syntax: "=Sheet1!C11"
* breakdown: = << name of sheet >> ! << cell id in original sheet >>
* clicking with mouse fills it in automatically

### 2.1.3.2.3 Pivot Tables
* A pivot table is a table of statistics that summarize the data of a more extensive table (such as from a database, spreadsheet, or business intelligence program). This summary might include sums, averages, or other statistics, which the pivot table groups together in a meaningful way. ~ [wiki](https://en.wikipedia.org/wiki/Pivot_table)
## 2.1.3.3 Preparation for Distribution
### 2.1.3.3.1 Identify Fields for Distribution
### 2.1.3.3.2 Suitable Names
### 2.1.3.3.3 Unicode - Special Characters
### 2.1.3.3.4 Remove Blank Lines
### 2.1.3.3.5 Data Dictionary
## 2.1.3.4 Ex. Checking Your Data (Checklist)
* add link to checklist right before class
