# Hackerank-Web-Automation

## Description

**Hackerank-Web-Automation** is a Node.js tool that automates the process of adding moderators to HackerRank contests. The main purpose of this project is to learn and demonstrate web automation using Puppeteer.

---

## Features
- Automates login to HackerRank.
- Navigates to the "Compete" section and manages contests.
- Traverses all contest pages and contests.
- Adds multiple moderators to each contest automatically.
- Handles dynamic navigation and input fields.

---

## Dependencies
- [`minimist`](https://www.npmjs.com/package/minimist): For parsing command-line arguments.
- [`puppeteer`](https://www.npmjs.com/package/puppeteer): For browser automation.
- [`fs`](https://nodejs.org/api/fs.html): Node.js built-in module for file system operations.

---

## Usage

1. **Install dependencies:**
   ```sh
   npm install minimist puppeteer
   ```

2. **Run the script:**
   ```sh
   node script.js --username <your-username> --password <your-password> --moderators <moderator-list-file>
   ```
   - Replace `script.js` with your main script filename.
   - The moderator list file should contain moderator IDs, one per line.

---

## Workflow

1. Open the browser using Puppeteer.
2. Get a new tab and go to the HackerRank URL.
3. Click login on the first and second pages.
4. Enter username and password on the third page and log in.
5. Click on "Compete" after logging in.
6. Click on "Manage Contests".
7. Determine the number of contest pages by inspecting navigation buttons.
8. Traverse all contest pages using the right-arrow navigation.
9. For each contest on a page:
    - Open the contest.
    - For each moderator:
        - Select the input field, type the moderator’s ID, and press Enter.
    - After adding all moderators, close the contest and move to the next.
10. Repeat for all contests on all pages.

---

## Learning Outcomes
- Practical experience with web automation using Puppeteer.
- Understanding of DOM navigation, event handling, and dynamic content.
- Practice with command-line argument parsing and file I/O in Node.js.

---

## Disclaimer
This tool is for educational purposes only. Please ensure you comply with HackerRank’s terms of service and use automation responsibly.
