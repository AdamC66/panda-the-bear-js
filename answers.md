1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
- PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

let profilePicture = document.querySelector(".profile-image")

profilePicture.src = "https://placebear.com/g/400/400"
"https://placebear.com/g/400/400"

2. Select the heading that says "Panda the Bear" and change it to your own name.

document.querySelector('h1.highlight').textContent="Adam Cote"

3. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

document.querySelector('.info-outter-container #employment h3').textContent="Werk History"

4. Change the colour of the body.

document.querySelector('body').style.backgroundColor='goldenrod'

5. Change the colour of each element using the highlight class. Use a for loop to do this.

for (i = 0; i < highlights.length; i++){
    highlights[i].style.backgroundColor = "lightblue"}
"lightblue"

6. Change the font family of the h1 to 'monospace'.
document.querySelector('h1').style.fontFamily = 'monospace'

7. Find a way to select the round icons in the sidebar and then change their colour.
let icons = document.querySelectorAll('.action-icon-bg')
undefined
icons[0].style.backgroundColor = "blue"
"blue"
icons[1].style.backgroundColor = "red"
"red"

8. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

document.querySelector('#name').placeholder="Identify yourself"
"Identify yourself"

9. Change the placeholder attribute of the message field to "state your business".

document.querySelector('#message').placeholder="State your buisness"

10. Give the name field a "value" attribute of "your nemesis".
document.querySelector('#name').value="Your Nemesis"

11. Change the value attribute of the email field to "koalathebear@gmail.com".

document.querySelector('#email').value="koalathebear@gmail.com"

12. Change the value of the submit button on the contact form to "En garde!".

document.querySelector('#submit').value="En Garde"

13. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

document.querySelector('#submit').disabled=true

14. We should help Panda protect their privacy by erasing their personal details from the sidebar.

let info = document.querySelector('.bio-info')
let bioinfoitems = document.querySelectorAll('.bio-info-item')
info.removeChild(bioinfoitems[1])
info.removeChild(bioinfoitems[2])


#Part 2
1. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

let pikachu = document.querySelector('#right-image')
pikachu.insertAdjacentHTML('afterend', pikachu.innerHTML)

let duppikachu2 = pikachu.cloneNode([deep=true])
pikachu.insertAdjacentHTML('afterend', duppikachu2.innerHTML)

2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

for(i=0; i<=10; i++){
    pikachu.insertAdjacentHTML('afterend', duppikachu2.innerHTML)}

3. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

const rightSpan = document.createElement('span');
var rightNow = document.createTextNode(new Date());
rightSpan.appendChild(rightNow);
listItem.appendChild(rightSpan);
theList = document.querySelector('.bio-info')
theList.appendChild(listItem)