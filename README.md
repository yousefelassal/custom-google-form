# Custom Google Form

### Get the pre-filled link
  
  ```html
  https://docs.google.com/forms/d/e/1FAIpQLSewfo9Dlptq7dVZeS9JK9iQCVirIi4-_KIqkKTXLA1NgTP6Fg/viewform?
  
  usp=pp_url&entry.1429682747=name&entry.1583891520=email&entry.191898897=phone&entry.333076107=website&entry.1200479729=message
  ```

  Extract the ids
  ```html
  entry.1429682747=name
  entry.1583891520=email
  entry.191898897=phone
  entry.333076107=website
  entry.1200479729=message
  ```
  
### Place link as form action
  change `viewform` to `formResponse`
  ```html
  <form action="https://docs.google.com/forms/d/e/1FAIpQLSewfo9Dlptq7dVZeS9JK9iQCVirIi4-_KIqkKTXLA1NgTP6Fg/formResponse">
    ...
  </form>
  ```

  add the `name` property to each one of our input fields and give them the value corresponding to the ids
  ```html
  <form action="...">
    <input
      placeholder="Your name"
      type="text"
      name="entry.1429682747"
    >
    <input
      placeholder="Your Email Address"
      type="email"
      name="entry.1583891520"
    >
    ...
  </form>
  ```
