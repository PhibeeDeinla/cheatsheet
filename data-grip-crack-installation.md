# DataGrip Installation (Crack version)

1. Download latest [DataGrip](https://www.jetbrains.com/datagrip/download/other.html) App or any JetBrains App
2. Copy and Paste `sniarbtej.jar` in any folder ex. `/Users/`
3. ex. DataGrip
   - look for `*.vmoptions` in `Applications/DataGrip/Contents/bin/` Folder
4. Edit `*.vmoptions` using any text editor then put this on the end of the line

- Specify the full path of `sniarbtej.jar`
  <br/> -javaagent:/Users/sniarbtej.jar=id=sniarbtej,user=Downloadly.ir,exp=2048-10-24,force=true

> Note:

- If Error `<app> Is Damaged and Can’t Be Opened. You Should Move It To The Trash` show on MAC upon opening the application. Type this on terminal<br/>
  `xattr -c <path/to/application.app>`
