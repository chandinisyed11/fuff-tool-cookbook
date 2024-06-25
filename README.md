# fuff-tool-cookbook
Description:
fuff is a powerful and flexible tool designed for fuzzing HTTP endpoints, particularly useful for web application security testing. It allows security professionals to discover hidden files, directories, parameters, and other vulnerabilities by sending numerous HTTP requests with various inputs. With its highly customizable and performant nature, fuff stands out as an essential tool in a security analyst's toolkit. Installation To install fuff, use the following command: go install github.com/ffuf/ffuf/v2@latest Ensure that Go is installed and properly configured on your system. (Or) We can simply use command : "apt-get install fuff".
Commmand: sudo apt-get install fuff

<img width="581" alt="image" src="https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/f0b24c18-d2ac-4530-8c1c-a409704c4991">

Or by using the another method to install fuff by using the url
With its highly customizable and performant nature, fuff stands out as an essential tool in a security analyst's toolkit. Installation To install fuff, use the following command: go install github.com/ffuf/ffuf/v2@latest Ensure that Go is installed and properly configured on your system. (Or) We can simply use command : "apt-get install fuff"

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/12b49e16-55db-438d-96b8-fea678edf5ae)

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/3c530589-4563-4af2-b5c0-98a9df868fe9)

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/5dbbd892-92d6-4129-924c-e15ee0738f66)

Usage of fuff:
1.Fuzzing Directories To fuzz directories on a website: "fuff -u https://example.com/FUZZ -w wordlist.txt" • -u: URL with the placeholder FUZZ where the payload will be inserted. • -w: Path to the wordlist file containing potential directory names.

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/476af523-190f-48d9-8257-99cb3789e182)

2.Fuzzing GET Parameters To fuzz GET parameters: "fuff -u https://example.com/page?FUZZ=value -w wordlist.txt"

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/1679fa82-cc2d-465a-9e66-9a5cb6f3332a)

3.Fuzzing POST Data To fuzz POST data: "fuff -u https://example.com/login -w wordlist.txt -X POST -d 'username=admin&password=FUZZ' " • -X POST: Specifies the HTTP method to use (POST in this case). • -d: Data to be sent in the body of the POST request.

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/4232209d-375e-40ed-ab10-0d2ce7a943b2)

4.Multi-Wordlist Fuzzing To use multiple wordlists simultaneously: "fuff -u https://example.com/FUZZ/FIZZ -w wordlist1.txt -w wordlist2.txt"

5.Using Filters To filter out results based on response status codes, sizes, or words: • Filter by status code: fuff -u https://example.com/FUZZ -w wordlist.txt -fc 404

• Filter by response size: fuff -u https://example.com/FUZZ -w wordlist.txt -fs 1234

• Filter by number of words in the response: fuff -u https://example.com/FUZZ -w wordlist.txt -fw 100

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/9e435fe1-3b94-4757-8819-5a63e29b0bda)

6.Recursion To recursively fuzz discovered directories: fuff -u https://example.com/FUZZ -w wordlist.txt -recursion

![image](https://github.com/chandinisyed11/fuff-tool-cookbook/assets/160826824/bdd4ee1a-cf10-45d3-9ce0-7062ae1bc90e)

7.Specifying Headers To specify custom headers: fuff -u https://example.com/FUZZ -w wordlist.txt -H 'Authorization: Bearer token' -H 'Custom-Header: value'

8.Output Options To save the output in various formats: • JSON: fuff -u https://example.com/FUZZ -w wordlist.txt -o output.json -of json

• CSV: fuff -u https://example.com/FUZZ -w wordlist.txt -o output.csv -of csv

9.Speed and Timing To control the speed and timing of requests: • Number of concurrent requests: fuff -u https://example.com/FUZZ -w wordlist.txt -t 50

• Rate limiting (requests per second): fuff -u https://example.com/FUZZ -w wordlist.txt -rate 100
