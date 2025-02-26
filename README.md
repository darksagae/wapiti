# wapiti
**Wapiti** is a web application vulnerability scanner included in Kali Linux. It allows you to audit the security of your web applications by performing various tests to identify vulnerabilities.

### Installation

Wapiti is typically pre-installed in Kali Linux. To check if it’s installed, run:

```bash
wapiti -V
```

If it's not installed, you can install it using:

```bash
sudo apt update
sudo apt install wapiti
```

### Basic Usage

The basic command structure for Wapiti is:

```bash
wapiti -u <URL> -o <output_directory>
```

- `-u <URL>`: Specifies the target web application to scan.
- `-o <output_directory>`: Specifies where the output reports will be saved.

### Example Command

To scan a web application, you can use the following command:

```bash
wapiti -u http://example.com -o /path/to/output
```

### Detailed Example with Options

You can also specify additional options, such as the type of vulnerabilities to scan for:

```bash
wapiti -u http://example.com -o /path/to/output --scope=all --ignore-robots
```

- `--scope=all`: Scans all URLs, including those disallowed by `robots.txt`.
- `--ignore-robots`: Ignores the `robots.txt` file.

### Expected Output

After running Wapiti, you will receive output similar to this:

```
[INFO] Starting scan on http://example.com
[INFO] Discovered URL: http://example.com/login
[INFO] Discovered URL: http://example.com/admin
[WARNING] Potential SQL injection vulnerability found in parameter "id"
[INFO] Scan complete: 150 URLs scanned, 5 vulnerabilities found.
[INFO] Report saved to /path/to/output/report.html
```

### Report Generation

Wapiti generates reports in HTML format in the specified output directory. The report includes:

- Identified vulnerabilities (e.g., SQL injection, XSS).
- A summary of the scan results.
- Detailed descriptions of each vulnerability found.

### Conclusion

Wapiti is a powerful tool for assessing web application security. It automates the scanning process and provides comprehensive reports on potential vulnerabilities. Always ensure you have permission to test any web application to comply with ethical standards and legal requirements.


                        ALTERNATIVE
**Wapiti** is a web application vulnerability scanner included in Kali Linux. It allows users to audit the security of their web applications by identifying potential vulnerabilities.

### Installation

Wapiti is usually pre-installed in Kali Linux. To check if it’s available, you can run:

```bash
wapiti -h
```

If it's not installed, you can install it using:

```bash
sudo apt update
sudo apt install wapiti
```

### Basic Usage

The basic syntax for using Wapiti is:

```bash
wapiti -u <target_url> -o <output_directory>
```

- `-u <target_url>`: Specifies the URL of the web application you want to scan.
- `-o <output_directory>`: Specifies the directory where the output files will be saved.

### Example Commands

1. **Basic Scan**:

   To scan a web application, use the following command:

   ```bash
   wapiti -u http://example.com -o /path/to/output
   ```

2. **Verbose Mode**:

   For more detailed output during the scan, run:

   ```bash
   wapiti -u http://example.com -v -o /path/to/output
   ```

3. **Scan with Specific Options**:

   You can specify certain options to customize the scan. For example, to include the detection of SQL injection vulnerabilities:

   ```bash
   wapiti -u http://example.com -m sql -o /path/to/output
   ```

### Expected Output

After the scan completes, Wapiti generates a report in the specified output directory. The report typically includes:

- **Found Vulnerabilities**: A list of potential vulnerabilities identified during the scan, such as SQL injection, XSS, and more.
- **HTTP Responses**: Details about the HTTP responses received during the scanning process.
- **Crawled URLs**: A list of URLs that were crawled during the scan.

### Example Output Snippet

When running Wapiti, you might see an output like this:

```
Starting scan on http://example.com
- Crawling: http://example.com
- Discovered: http://example.com/login
- Discovered: http://example.com/register
- Potential SQL injection found in: http://example.com/login?id=
- Scan completed. Vulnerabilities found: 2
```

### Conclusion

Wapiti is a robust tool for identifying vulnerabilities in web applications. It provides detailed reports that can help security professionals prioritize remediation efforts. As with any security tool, ensure you have permission to test any web application to comply with legal and ethical standards.



                          ALTERNATIVE
**Wapiti - Web Application Vulnerability Scanner in Kali Linux**

Wapiti is a free and open-source web application vulnerability scanner included in Kali Linux. It is designed to discover security vulnerabilities in web applications, such as SQL injection, cross-site scripting (XSS), and file inclusion.

**Usage**

The basic syntax for using Wapiti is:

```
wapiti [options] <target_url>
```

Some common options include:

- `-o <output_dir>`: Specify the output directory to save the scan results.
- `-m <modules>`: Select the modules to use for the scan (e.g., `sql,xss,exec`).
- `-f <file>`: Specify a configuration file.
- `-t <threads>`: Set the number of concurrent threads to use.
- `-v`: Increase the verbosity of the output.

**Example Commands**

1. **Basic Scan**:
   ```
   wapiti -o /path/to/output http://example.com
   ```
   This command will perform a basic scan of the `http://example.com` website and save the results in the `/path/to/output` directory.

2. **Scan with Specific Modules**:
   ```
   wapiti -o /path/to/output -m sql,xss,exec http://example.com
   ```
   This command will scan the `http://example.com` website for SQL injection, cross-site scripting, and code execution vulnerabilities, and save the results in the `/path/to/output` directory.

3. **Scan with Custom Configuration**:
   ```
   wapiti -o /path/to/output -f /path/to/config.xml http://example.com
   ```
   This command will use a custom configuration file (`/path/to/config.xml`) to perform the scan and save the results in the `/path/to/output` directory.

**Example Output**

The output of Wapiti will be saved in the specified output directory. The directory will contain several files, including:

- `report.html`: An HTML report summarizing the scan results.
- `report.txt`: A text-based report of the scan results.
- `report.xml`: An XML-formatted report of the scan results.

The report provides information about the target website, such as:

- Identified vulnerabilities (e.g., SQL injection, XSS, file inclusion)
- Detailed descriptions of the vulnerabilities
- Recommendations for remediation

Here's an example of what the output might look like:

```
[+] Starting scan of http://example.com
[*] Checking for SQL injection vulnerabilities
[*] Found potential SQL injection vulnerability in parameter 'id' at http://example.com/product.php?id=123
[*] Checking for cross-site scripting (XSS) vulnerabilities
[*] Found potential XSS vulnerability in parameter 'search' at http://example.com/search.php?search=test
[*] Scan complete
[+] Issues found:
    - SQL injection (2 occurrences)
    - Cross-site scripting (XSS) (1 occurrence)
[+] Report saved to /path/to/output/report.html
```

**Conclusion**

Wapiti is a powerful and versatile web application vulnerability scanner that can help identify security issues in your web applications. By using various modules and configuration options, you can customize the scan to fit your specific needs.





                             ALTERNAIVE
Wapiti is a web application vulnerability scanner that is included in Kali Linux. It is used to identify vulnerabilities such as SQL injection, cross-site scripting (XSS), file inclusion, and more in web applications.

**Basic Usage:**

The basic syntax for using Wapiti is:
```
wapiti -u <target_url> -o <output_file>
```
* `-u <target_url>`: Specifies the URL of the web application to scan.
* `-o <output_file>`: Specifies the file to save the scan results to.

**Example Usage:**

1. **Basic Scan**:
```
wapiti -u http://example.com -o output.txt
```
This command will perform a basic scan of the `http://example.com` website and save the results to a file named `output.txt`.

2. **Scan with Authentication**:
```
wapiti -u http://example.com -a username:password -o output.txt
```
This command will perform a scan of the `http://example.com` website with authentication credentials `username` and `password`, and save the results to a file named `output.txt`.

**Example Output:**

The output of Wapiti will include a list of identified vulnerabilities, including:

* SQL injection vulnerabilities
* Cross-site scripting (XSS) vulnerabilities
* File inclusion vulnerabilities
* Authentication and authorization issues
* Other security issues

Here's an example of what the output might look like:
```
**Vulnerabilities found:**

* SQL Injection:
	+ Parameter "id" is vulnerable to SQL injection
	+ Parameter "username" is vulnerable to SQL injection
* Cross-Site Scripting (XSS):
	+ Stored XSS vulnerability in parameter "comment"
	+ Reflected XSS vulnerability in parameter "search"
* File Inclusion:
	+ Potential file inclusion vulnerability in parameter "file"
* Authentication and Authorization:
	+ Authentication bypass vulnerability in login form
* Other security issues:
	+ Potential information disclosure in error messages
```
**Important Notes:**

* Wapiti should only be used with permission from the web application owner.
* Wapiti is a powerful tool that can potentially cause damage to a web application if used improperly.
* It's essential to review the scan results carefully and prioritize vulnerabilities based on their severity and impact.


                           ALTERNATIVE
**Wapiti** is a web application vulnerability scanner included in Kali Linux. It is designed to audit the security of web applications by performing "black-box" scans, meaning it does not analyze the source code but instead tests the web application by interacting with its pages and forms.

### How to Use Wapiti

1. **Installation**:
   Wapiti is typically pre-installed in Kali Linux. If you need to install it, you can do so using:
   ```bash
   sudo apt-get install wapiti
   ```

2. **Basic Command Structure**:
   The basic syntax for running Wapiti is:
   ```bash
   wapiti -u <target_url>
   ```
   - `-u <target_url>`: Specifies the URL of the web application you want to scan.

3. **Example Usage**:
   Here are a few examples of how to use Wapiti:

   - **Basic Scan**:
     To perform a basic scan on a target website:
     ```bash
     wapiti -u http://example.com
     ```

   - **Verbose Mode**:
     To run Wapiti in verbose mode, which provides more detailed output:
     ```bash
     wapiti -v2 -u http://example.com
     ```

   - **Output in HTML Format**:
     To generate a report in HTML format:
     ```bash
     wapiti -u http://example.com -f html -o /path/to/output/report.html
     ```

   - **Specify Scan Level**:
     You can specify the level of the scan to control the depth of the testing:
     ```bash
     wapiti -u http://example.com -l 3
     ```

### Expected Output

After running a scan, Wapiti will generate a report that includes:

- **Vulnerabilities Found**: A list of potential vulnerabilities such as SQL injection, XSS, and others.
- **Scan Summary**: Information about the number of URLs scanned and the types of vulnerabilities detected.
- **Detailed Report**: If you specified an output file, you can open it in a web browser to view detailed findings.

For example, when scanning a site, you might see output like this:

```
[INFO] Starting scan on http://example.com
[INFO] Found potential SQL Injection vulnerability in parameter 'id'
[INFO] Found potential XSS vulnerability in parameter 'name'
[INFO] Scan complete: 150 URLs scanned, 2 vulnerabilities found.
```

### Conclusion

Wapiti is a powerful tool for identifying vulnerabilities in web applications. By using various command options, you can customize your scans and generate detailed reports to help improve the security of your applications.

---
Learn more:
1. [Using Wapiti Web Scanner To Secure Your Web Applications](https://linuxsecurity.com/features/features/complete-guide-to-using-wapiti-web-vulnerability-scanner-to-keep-your-web-applications-websites-secure)
2. [wapiti | Kali Linux Tools](https://www.kali.org/tools/wapiti/)
3. [Wapiti -- Automated Vulnerability Scanner](https://www.kalilinux.in/2021/01/wapiti-tutorial.html)
