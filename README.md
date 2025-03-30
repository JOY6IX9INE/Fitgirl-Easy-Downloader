# Fitgirl-Easy-Downloader
This Tool Helps To Download Multiple Files Easily From fitgirl-repacks.site Through fuckingfast.co

## Prerequisites
Ensure you have the following installed before running the script :
- Python 3.8+
- Required Python packages :
  - `requests`
  - `beautifulsoup4`
  - `tqdm`
  - `colorama`


## Usage
1. **Prepare Input Links** : Add your URLs to `input.txt`, one per line.
2. **Run the Script** :
   ```bash
   python main.py
   ```
3. The script will :
   - Process each link in `input.txt`.
   - Extract and download files to the `downloads` folder.
   - Remove processed links from `input.txt`.

## Extra  

To extract and copy all direct download links, follow these steps:  

1. Open the page where you want to grab the links.  
2. Open the **browser console**:  
   - **Windows/Linux:** Press `F12` or `Ctrl + Shift + I`, then go to the **Console** tab.  
   - **Mac:** Press `Cmd + Option + I`, then go to the **Console** tab.  
3. Paste the script below into the console and press **Enter**.  
4. All matching links will be displayed and automatically copied to your clipboard!  

````js
(() => {
    const links = Array.from(document.querySelectorAll('a'))
        .map(a => a.href)
        .filter(url => url.startsWith('https://fuckingfast.co/'));

    if (links.length === 0) {
        console.log("❌ No Matching URLs Found");
        return;
    }

    console.clear();
    console.log("🔗 Matching URLs :\n");
    console.log(links.join("\n"));

    const textarea = document.createElement('textarea');
    textarea.value = links.join("\n");
    document.body.appendChild(textarea);
    textarea.select();

    try {
        document.execCommand('copy');
        console.log("\n✅ All Links Copied To Clipboard!");
    } catch (err) {
        console.error("❌ Failed To Copy :", err);
    }

    document.body.removeChild(textarea); 
})();
````  

# Disclaimer
This tool is created for educational purposes and ethical use only. Any misuse of this tool for malicious purposes is not condoned. The developers of this tool are not responsible for any illegal or unethical activities carried out using this tool.

[![Star History Chart](https://api.star-history.com/svg?repos=JOY6IX9INE/Fucking-Fast-Multi-Downloader&type=Date)](https://star-history.t9t.io/#JOY6IX9INE/Fucking-Fast-Multi-Downloader&Date)
