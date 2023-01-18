# Installing PostgreSQL, PostGIS, QGIS, and GRASS GIS
We will be using several other open source softwares for analysis throughout the semester. You'll need to get those installed before your can use them.

## Contents
1. <a href="#install-postgresql-and-postgis">Install PostGreSQL and PostGIS</a>
2. <a href="#install-qgis-gdal-and-grass-gis">Install QGIS, GDAL, and GRASS GIS</a>

## Install PostGreSQL and PostGIS

<table><tbody><tr><td colspan="2">
  <ol><li>You may have a version of PostgresSQL which is older than 15.1 and an older version of PostGIS. Check with Control Panel and uninstall the old version, if needed (be sure to uninstall PostGIS first and PostgreSQL second). Uninstalling won't delete your old data folder, but it can help conflicts coming up with installing a new version.</li>
  <li>Install the newest version of PostgresSQL by walking through the Installer, taking these parameters:</li>
    <ol><li>Install directory: default</li>
      <li>Select components: ALL</li>
      <li>Data Directory: Your choice, but keep it on the C drive. I elected to put it in my C:\Users\Jennifer\Documents\PostgresSQL\data folder, mostly because that is where I have the majority of my GIS data (I had to make two new folders - PostgresSQL and data).</li>
      <li>Super User password: something you will for sure remember!!!!</li>
      <li>Port: 5432 (default)</li>
      <li>Advanced Options Locale: Default Locale</li></ol></ol></td></tr>
 <tr><td><ol start="3">  
    <li>Once the PostgresGIS installer finishes, it will offer you the choice to launch Stack Builder. Make sure the box is checked and click Finish</li><ul><li>If you closed the installer without launching <em>Application Stack Builder</em>, you can re-open it by looking for it in the Start menu. You would also do this if you needed to install new packages at a later date.</li</ul></td>
   <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEWq6hCz5OAixpt8q2l_b3QA7IGbhdV8Zx5oVTqVzN6LwEeUQ0HZgCLh0rkzmcaRcetRkiniZL36baUcsM-w4IdpuguqhhaMk7JiZSteq21RlXpTcOmfHHEkvub_EFmvo_1FuRUnTG0bU0GTJRwv5qgW=w552-h432-no?authuser=0" /></td></tr>
 <tr><td><ol start="4">  
   <li>Select PostgreSQL 15 on port 5632 dropdown.</li></ol></td>
   <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEVrABdMTmnNdZjHxeUV0zXxqakFh6IfTe4ouKXWPbOROhplDnY-TkOWsYVfGUJW61ODvHb3-mrbaEo8zbkcVW0c0WDZdueuRH9LmuKSR_1ndGozNcNd_OYxxhyKg-4vvH7AA5akiI3tjP0_AThDWbrF=w611-h419-no?authuser=0" /></td></tr>
 <tr><td><ol start="5">  
   <li>Expand the <strong>Database Drivers</strong> and select: <ol><li>Nqgsql, <li>pgJDBC, and <li>psqlODBC(64bit)</li></ol></li>
   <li>Expand the <strong>Spatial Extensions</strong> and select:<ol><li>PostGIS 3.3 Bundle for PostgreSQL 15</li></ol></li>
   </td>
   <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEXvcoXSWNEVGVZmiG5rePXC4W9tzbitTnkSV4zuE7_tqJgjyfWkuytjXWwTu_-mzqEfYH8Uqdl4iuxh0fcyLc8nk2ZLBRccO_XgnfX0X-IBUGj5fbu67XbiD1A0uVX2oIzDFvHsXju50-z_NgvFjLJi=w611-h419-no?authuser=0" /></td></tr>
 <tr><td><ol start="6">  
   <li>Allow the installer to download the extensions and click Next to install them (defaults are just fine)</li></ol></td>
   <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEURGapxD2Y21gYD4AW_u7S6qUlozN7Om3HxroQfW6P57urGBDGj1N0LLNwU77qs1tzIhSw4kPNupjnxYGY1h8hSvicsfEQo8_zxZeyyka4m1cRMQiS_POkMud7m8fTKlgtTnny5mCHyyuAck1h2QJVJ=w611-h419-no?authuser=0" /></br><img src="https://lh3.googleusercontent.com/pw/AL9nZEULJT37PT0byfOz6IabmCIiD7K79NBY4r7CFVnR69E42ghAv4I4yN_GkpnflIE-O32t4dWKcb429p1gn2CB6VThZSlmjBxwBLUBgZ_zuAgWe0NQgDzB454zDo9DbahvJDqb3KL5rKR9Tq-tRLcDiW2s=w611-h419-no?authuser=0" /></td></tr>
 <tr><td colspan="2"><ol start="7">  
   <li>Each of the three database extensions will ask you to install them seperately. Go ahead and do this task. It will consist of three screens each. Wait between each one as the next one launches. You may need to open the installer from the taskbar.</li></td></tr>
  <tr><td><ol start="7">  
  <li>PostGIS Bundle for PostgreSQL will ask to be installed. This is a very important extension to be installed!</li></ol></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEXQuQAcuNXvSNhgofOazT4YBSckKIOvP-lVTAFpyA_GVqWvZSr3XSsqpcQKMJp1fSerYP4Yz6UhsTPA7CvD3hcS0mhILU8L2wWfSVCykxpfudX3yUypk4sh89TlQwyfGjcyexXAz814OWtPt4DJQvkY=w499-h388-no?authuser=0" /></td></tr>
  <tr><td><ol start="8">  
  <li>Allow PostGIS to create a sample spatial database and hit next.</li><li>Allow the destination foler to be the default (this is the install directory for the extension, not the data) <em>Not shown</em></li></ol></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEVxbjoaVbQhs1Mgnxg8QkjkEM26rrWf3xfNr_k4fAZAbhpj00dvSUIIukBEYIfwKLTPI18MmGgigSGYaAVRQsPRFuIxuyCHc2VZT3jQ8QI96hZen687jrpr0onboJVr-JdaDNThKLOU3rKqJbXOD2BQ=w499-h388-no?authuser=0" /></td></tr>
  <tr><td><ol start="7">  
  <li>Enter the password you created in Step 2. I told you not to forget!</li></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEWpeXdixSXF2gTF2lB4v2pAuHzaa7WnXX38i4ttjMYQ0QChNCr4Ti03U9iDO4NIK_4SfAuaSOKxSrbt7olEYQFdVvM6J6vUehY1FLT5DJhYYCRmsvJvB4yvqVUIdMgk-jGUQ9cV-I5E3VYLYq4FzQrP=w499-h388-no?authuser=0" /></td></tr>
    <tr><td><ol start="7">  
  <li>Name the database "gis-3011-geopandas". We will be using this first database during Assignment Two.</li></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEUjqsDAelon9VmWA-sWqC4NFaGnDZ1T0z5vc1SCqhvnC1BxWPyezO1oHaBODaJ1iEwyoooVV-zvDZ4LPrpQNpMu8PdFLYW6jAvafmNGYGxu5-M2B5IcfbALZS2tRO7ULJMPS0WV4i9IgyZChd4f-7Qr=w499-h388-no?authuser=0" /></td></tr>
    <tr><td><ol start="7">  
  <li>You'll be asked to confirm 3-4 options about database environments and enabling extensions. Click YES for all of them.</li></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEXqOFZFgtfUTbWSUbYlxUAit5CMFksturOJORbepvKKofB3hx9PFbzuyA_h5gYoIQxwXRbltiCx1dLTYLW7eNgliytX5qhszabMHYFrPlWqorPuGEXDFa1pS-EDwp4JWhnrQD9v3Rdus1fXH0_LXp6-=w409-h154-no?authuser=0" />
  </br><img src="https://lh3.googleusercontent.com/pw/AL9nZEX2Ou0Te7o177roxIrPif5EEa_QoxC7GR6w8mr6IAwP0T-QNzdP4Yvg_0lRIyoZG9bQp6HkGYMqIFg27qUiRXtRg5L2S-EZ5hXP7bzTVRlmNUSJRETABNjsvNS0AxEmZlojOusm4V-ft5w6if3fgxUR=w407-h154-no?authuser=0" />
  </br><img src="https://lh3.googleusercontent.com/pw/AL9nZEUXqQlHZfJqpKB6rJagEiNWgnT4i7KDY82tXzoq_88B_EhT-Nv8ZRnPmmDm_UpMElb1edM-lP4HUGPhuJtvXJvE1_CPfc_io7t_-8N9YPPdKOI3BcA16rbNOjzIr-q1yWPIUp04n59rxNtDpLCzYrFh=w407-h180-no?authuser=0" />
  </br><img src="https://lh3.googleusercontent.com/pw/AL9nZEWWNLRYLr_jkoUk4wuEmH30dkfsEcnO1kdKs08tNLV7yx5MUwMdNRnOkFPUN7tWUIQFhdH5flIe-uZD7hDlEriuFuRGPjyVRk0qML2Iwyq90O2WvdEu0pECeiVD3SIGoyBxDYuvQ0Q6gNluzgp4M6tJ=w400-h154-no?authuser=0" /></td></tr>
   <tr><td><ol start="8">  
  <li>Close the PostGIS installer when it's finished</li></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEVo0V7TMs1jlEctzN5WrUGr5RqGWjnHAz-WFN2kwqddlBaXvOtmfCnFg6_yjWly35R56tK7qTdiaFEtXw8k_h2IkO5zCyhwJKuJpoSv1jsOo9IAZwbvG9DIfqNPWfJUpjTT9bhei3uJ-rdZ8CPWnAI5=w499-h388-no?authuser=0" /></td></tr>
     <tr><td><ol start="9">  
  <li>Click Finish on the Stack Builder installer window</li></td>
  <td><img src="https://lh3.googleusercontent.com/pw/AL9nZEWfr2YN9UuRSq42d3McTTJuh7HEA6np8NX099GbMZ2IeOiD9oVIf5RPcD1HyjtYHB9gk5VfqUNV0lwsiEGbE8kdM4E6rFbZaR4Zn0sDBtNBflOfYMXGJH6pQszezIzWgSqeXaP5crkfELp5qQ2XG9Bs=w611-h419-no?authuser=0" /></td></tr>
<tr><td colspan="2">
  <ol start="10"><li>Find and launch <strong>pgAdmin</strong> in the start menu. It will ask again for the master password. Enter it and click OK. If everything opens and you can see the new gis-3011-geopandas database, your golden.</li></td></tr>
</tbody></table>
  
## Install QGIS, GDAL, and GRASS GIS
  
<table><tbody><tr><td colspan="2">
  <ol>   
   <li>Visit https://trac.osgeo.org/osgeo4w/ and download the OSGeo4W network installer file</li>
   <li>Once downloaded, <strong>RIGHT CLICK AND RUN AS ADMINISTRATOR</strong> (it may not do it automatically)!</li></ol></td></tr>
<tr><td style="width:60%;">
  <ol start="3"><li>Select Express Install</li></td></tr>
  <tr><td style="width:60%;"><ol start="4">
    <li>Select the link for download.osgeo.org</li></td></tr>
  <tr><td style="width:60%;"><ol start="5">
    <li>Check off QGIS, GDAL, and GRASS GIS</li></td></tr>
  <td colspan="2"><ol start="6">
    <li>Finish up the install, taking the remaining defaults</li></td></tr>
  </tbody></table>
