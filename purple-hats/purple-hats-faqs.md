# FAQs

The following section provides frequently asked questions related to Purple Hats. 

>**Tip:** Click on a question to view the answer.

<details>
  <summary><b>How do I limit number of pages scanned?</b></summary><br>

If you find a scan takes too long to complete due to large website, or there are too many pages in a sitemap to scan, you may choose to limit number of pages scanned.  

To do this:  
1. Open `constants\constants.js` with a text editor.  
1. Change the value `exports.maxRequestsPerCrawl` to a smaller number, e.g. `exports.maxRequestsPerCrawl = 10;`
1. Save the file.  
1. Start a new purple-hats scan.  

</details>
