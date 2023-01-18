# Installing Git, Creating an Access Token, and Cloning your First Repository with the GitHub Bash Window
Git and GitHub will be used to clone assingments, create assignment repositories, and create versions of your assignments through the semester.

<table><tbody><tr><td colspan="2">
<ol><li>Visit https://git-scm.com/download/win and download the latest 64-bit build for windows
  <li>Install or Update Git, taking all the defaults</ol></td></tr>
<tr><td>
  <ol start="3"><li>Back at Github.com, sign in and click on Settings under your account dropdown (upper right of the GitHub window)</td><td>
<img  src="https://lh3.googleusercontent.com/pw/AL9nZEV7OZS9rP6dKemGXc8WxS3iLO8JfeOgJizDBROP80BmX4BNwpkaNVoKPrL4C2lvOkpnshsiDsU_JCaouSEtKSZalJvUBksKY7TwSVCQi8lqHdsj_yS9nUP735b7zHxR7uvXJ1HW7pRAO_lpSfwxkwoF=w536-h631-no?authuser=0" /></td></tr>

<tr><td><ol start="4"><li>Go to the developer Settings (last option in the left list)
<li>Click on <strong>Personal Access > Tokens Tokens (classic)</strong>, then <strong>Generate a New Token > Generate New Token (classic)</strong></td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEUuxQXDw6TmbUqNUHAeFx9WlN7am-ack0UvNumA9HBbXTDLgG8xeJqWaj5OBoahDdTdw2DCRWLYS5m7tmH2WAEEYHHe5_RAWWHrgOSlD8WPlAg2CD-_ppUs_QfkGRmEHAWIKu3llq8NVP2feCcLb5Lc=w1164-h454-no?authuser=0" /></td></tr>

<tr><td><ol start="6"><li>Name the token <strong>gis-3011-sp-2023</strong> and set the expiration date to <strong>Custom > May 10, 2023</strong>
<li>Check off the boxes for - <strong>repo, admin:repo_hook, and delete_repo</strong>
  <li>Click on <strong>Generate Token</strong></td><td><img src="https://lh3.googleusercontent.com/pw/AL9nZEUMh9U9mMHxxyv8e25pcVTB5D3MV22MQ-6AOb_lR7DIM_w2yBtG4agKwcUdOUC6BxSMWWlv0HkAuvPVrD8A8T3dvXH9Z0-wcoqL-Idh1voLTmRxW0u-D1OawH_vj4pUm7NsuBkBgfFk0jP5LJiljGhs=w788-h949-no?authuser=0" /><img src="https://lh3.googleusercontent.com/pw/AL9nZEUsw-3VlOkOhPNnmBI3tBFSvovvO1fQpZLLnEOdbh-o_YymtspgMjOkfDbxhWJzbvWDuE-vaVh0u2aViC7qLbZGYJwuYPlAKMtLT0llPdK-oeF9uNQfdGAeXCpJtNgNN2ZTEkmskeYLnmVDuCOvOnbj=w789-h621-no?authuser=0" /></td></tr>
    
<tr><td><ol start="9">    
<li>When the token appears, copy it (DON'T CLOSE THE PAGE YET!) and open a new text document in your GIS-3011 folder (or whatever your called it - you will need this folder for many things!). Save the token to the text document. 
<ul><li>If you ever lose the token, you can just make a new one, so it's not the end of the world</ul></ol></td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEWgR_QJdNW9iDKygsdD32izp_VK2t9PmIrdxPp1WwpwTHWYrqZK2Yrz8J92jCh2AZIQDCyBsdH6uqs6kVExOfsqjRhJs9vkbBw-_gKW5Wijmj1TS_KlSUu-ctEAnE_l8yfAdaFc_jiyKDQ8FJrDIxo3=w1134-h320-no?authuser=0" />
</td></tr>
     <tr><td><ol start="10"><li>On github.com, go back to your main page and open your repositories and then open the Setting Up Your Environments respository.</li>
       <li>Drop down the green CODE button and copy the address from HTTPS</td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEUMjHg8sfB9lexMCC4VUQeKU6enPcBQ_J0DNAEScwd0WVd4DnXzcYMk8QyrrYhacFVWbuTKt-20oE00UUkK7bt5FmuuVT82X8_oMi4osbOHWLF4qBNHneQzSd4gjBl1mzUCdwqrYqLLbrpcTgd8x_1I=w1896-h754-no?authuser=0" /></td></tr>
  
  <tr><td><ol start="12"><li>From the Start Menu of your computer, launch Git Bash</li></td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEXBnjuDWdgoIuiKFkZjMPWSveeQEjSdeEe5nBOp7iV6A2ARMFGCdfuuQJMqDNGaNO303B5BiXL8MQeTjYTqh7bFMWYzJ3dWSdwM_jo8mkxHgeOl7od-u37Ffvl41rM1XZCqkuCSsAjf0bavzMY5iO3s=w833-h681-no?authuser=0" /></td></tr>
   
  <tr><td><ol start="13"><li>Use the <code>cd </code> command to open your GIS-3011 folder. <ul><li>Your path may vary from mine! Since I'm using my Documents folder and the GitHub bash defaulted to my C://Users//Jennifer folder, I only had to move two folders.</li><li>It's possible to paste a path in the GitHub Bash, but you'll need to either right-click and paste or use Ctrl+Shift+V.</li></td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEVpZYdj9qTAalWBV-6ItQObr-lycUNfTMihcRIGLr5lzccJFx440-V3I83HPYxwvYcBy0LMOlMORwOsGuFpRc9MCZUn4_DCPKamgA5vX4_uJdU_ebOwRhgNQqnmLuTH10VOvcdA9miUJbQZl60A98im=w882-h370-no?authuser=0" /></td></tr>
    <tr><td><ol start="14"><li>Once you're in your GIS-3011 folder, use the command <code>git clone https://github.com/jennifer-muha/setting-up-your-environments.git</code> (but obviously your GitHub address!) and press enter.</li></td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEXqxaXLQvmK60yoTXpOZxU-5Rii7KcPDe7P34GCo0v2y9gOHkR5VYPKPEjJENDKhiW-bA1rgBToa9FQ9asDutM5AWDCAL-Azqf4H8F8v-oygqpv59I-X1VvBYosV0xoKI41AO6Y6bnIRwjaWMKcOPUa=w882-h370-no?authuser=0" /></td></tr>
    <tr><td><ol start="15"><li>Once the respository successfully clones, the bash window will let you know and you'll see the folder stored locally on your computer.</li></td><td>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEV7TlFvr2PHxAKsLQq_f-YG11kaHVdRGOFPuFeMxNxjDMpgMT1ZjGnNFTlh7N8Clw2MhgGeJ2qtCzSUDnQndO8RfM-FySmDQPe01RZCOe-YRSqhBOc8Sza5nwVez0jmc98DFHgwHDsvLmZRlzYB89Le=w882-h370-no?authuser=0" /></td></tr>
</tbody></table>
