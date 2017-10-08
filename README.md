# Bibliographic-dataset
This repository contains a sample of scientists with their complete citation and collaboration graphs as retrieved from MAS and the complete information on their citers and collaborators as well. This results in complete graphs (publication, citation and collaboration) around an initial sample of authors allowing for bibliographic analysis across multi-layer graphs. The complete dataset can be obtained upon request (agogoglou@csd.auth.gr)

The first compressed file-fromHeidiCoA.txt.tar.bz2-contains a .txt file with the collaboration network around a sample of 10 core-scientists. 
The columns in each row are the following: 
msauthor_id,r_msauthor_id,title,doi,n_authors,pub_type,year_e,msjournal_id,CoAuthorIDs,CoAuthorIDsMerged,CoAuthorsPublications,CitingPubsOfCoAuthorsPubs

The above columns explained:
* **msauthor_id:** the unique identifier of a core-scientist
* **r_msauthor_id:** merged IDs in case of scientists with multiple name variations
* **title:** title for publications of the core-scientist
* **doi:** DOI for publications of the core-scientist
* **n_authors:** number of authors for publications of the core-scientist
* **pub_type:** type of publication (conference/journal) of the core-scientist
* **year_e:** year of publication of the core-scientist
* **msjournal_id:** journalID for publication of the core-scientist (0 if conference)
* **CoAuthorIDs:** ID of scientist that coauthored this publication with the core-scientist
* **CoAuthorIDsMerged:** merged IDs in case of coauthors with multiple name variations
* **CoAuthorsPublications:** IDs of publications authored by the coauthors of the core-scientist
* **CitingPubsOfCoAuthorsPubs:** IDs for publications citing the coauthors' publications 

The second file is divided into 5 compressed files: compressed.gzaa,compressed.gzab, compressed.gzac, compressed.gzad, compressed.gzae
To uncompress into a single file use the following command:
$ cat compressed.gz* | zcat > /path/to/decrompressed/file

The resulting uncompressed .txt file will contain rows with the following columns:
authorID, r_authorID, pubID, pubTitle, pubDOI, pubNumOfAuthors, pubType, pubYear, pubJourID, citingPub, authorID_citingPub, authorFirstName_citingPub, authorLastName_citingPub, pubID_citingPubAuthor, pubTitle_citingPubAuthor

* **authorID:** the unique identifier of a core-scientist
* **r_authorID:** merged IDs in case of scientists with multiple name variations
* **pubID:** IDs for publications of the core-scientist
* **pubTitle:** title for publications of the core-scientist
* **pubDOI:** DOI for publications of the core-scientist
* **pubNumOfAuthors:** number of authors for publications of the core-scientist
* **pubType:** type of publication (conference/journal) of the core-scientist
* **pubYear:** year of publication of the core-scientist
* **pubJourID:** journalID for publication of the core-scientist (0 if conference)
* **citingPub:** ID of publication that cites the respective one of the core-scientist
* **authorID_citingPub:** author ID for the citing publication (citing author of the core-scientist)
* **authorFirstName_citingPub:** first name of the citing author 
* **authorLastName_citingPub:** last name of the citing author
* **pubID_citingPubAuthor:** ID for other publications authored by the citing author
* **pubTitle_citingPubAuthor:** title for other publications authored by the citing author
