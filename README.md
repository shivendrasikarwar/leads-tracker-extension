
# Chrome extension leads tracker




## Overview

- Save leads writing them into the input element
- Save the current Chrome tab in the list
- Maintain leads even after closing the browser
- Delete all leads by double clicking on the last button


## 🔗 Links

Live Site URL @:  [ Live Site URL](https://shivendra-github.github.io/leads-tracker-extension/)


## Tech Stack

**Javascript:** Json, localStorage, DOM

**CSS:** Flexbox, Mobile-first workflow

**HTML:** HTML5

**API:** Google Chrome APIs


## What I learned

- How to get the active Chrome tab and store it into localStorage using JSON's methods

```bash
  tabBtn.addEventListener("click", function () {
  chrome.tabs.query({ active: true, currentWindow: true }, function (tabs) {
    myLeads.push(tabs[0].url);
    localStorage.setItem("myLeads", JSON.stringify(myLeads));
    render(myLeads);
  });
});

```





- How to use "template string" with backtick manipulating directly the DOM
```bash
function render(leads) {
  let listItems = "";
  for (let i = 0; i < leads.length; i++) {
    listItems += `<li>
                        <a target="_blank" href="${leads[i]}">
                        ${leads[i]}
                        </a>
                </li>`;
  }
  ulEl.innerHTML = listItems;
}

```
## Authors

- [@shivendra](https://www.linkedin.com/in/shivendra-pratap-singh-123408233/)


## Acknowledgements

 - A big thank you to [Per Harald Borgen](https://github.com/perborgen) for helping me out to buit this project 👏


