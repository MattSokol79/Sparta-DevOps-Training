# Day 2 - Setting up Git and Communication
Notes of all aspects covered on Day 2

## Trello
- Used to track the training progress, what we will cover and when
- Refer back to the board to find relevant topics for revision

## Git
### Setup + SSH Key
- Downlaod GitBash on Windows
- Run GitBash whenever needing to use Git
- Make a folder somewhere you know by `mkdir (Foldername)`
- `cd` to the folder of your choosing
- E.g. `cd (Foldername)`
- Generate a key
- `ssh-keygen -t rsa -b 4096 -C "your_email@email.com"`
- Check the key exists with `ls` in the folder it is saved in
- Access the key by `cat (Foldername)` then copy and paste this into GitHub
- Go to GitHub and go to `Settings`
- "SSH and GPG Keys" => "New SSH key"
- Paste the SSH key copied earlier into the New SSH key window and add a title
- Back in GitBash test SSh
- `ssh -T git@github.com`
- When RSA key fingerprint question comes up => `yes`
- If Successful it will say

### Repositories
- Make a repository within GitHub
- Within the created folder earlier in bash `git init` to initialise a repo
- If there are files present within the folder use `git add (FIle name)`
- Instead if you want to add all files `git add .`
- To make a file either `touch Filename.format` e.g. README.md or immediately start editing it with `nano Filename.format`
- Within `nano` Save `Ctrl + X` and then `y` and `Enter` to leave the editing
- Commit the file with `git commit -m "commit name"` => commits all files
- `git branch -M main` Makes the "main" branch
- `git remote add origin git@github.com:USER:NAME/REpo_name.git` => Link the folder to github repo
- `git push -u origin main` => Upload the files
- If you make any changes or make another file, add those files again, commit and push

### Notes
- Possibly utilise VSC instead of nano for ease of use in later coding
- GitHub Desktop may be easier to use as well

## Business Skills - Communication and Time Management

### How to manage your time well with the tools that we have?
- Use the calendar/weekly planner provided by outlook or teams
- Utilise the Trello to understand what tasks you have to do and what to revise

Task management - the process of managing a task during its lifecycle including planning tracking and reporting

1. Prioritise Well
2. Set time boundaries
3. Organise routinely
4. Plan ahead
5. Stay focused

### Eisenhower and Pareto Principles

- Eisenhower principle follows the principle of the eisenhower decision matrix (Pic). It is a way he organised his workload and
priorities. Great time management means being effective as well as efficient. It helps you identify acitiveis that you should
focus on and those that you should ignore.
I.e. Urgent + Important = Do it now, Not urgen + important = Schedule a time to do it etc. etc. refer to matrix

- Pareto Principle is the idea that 80% of the result comes from 20% of the input so e.g. 20% of the bugs contribute to 80% of
crashes. The point is to realise that you can often focus your effort on the 20% that makes a difference.

### Other notes on managing your time
- Be disciplined, remove temptations dont make it hard on yourself
- Care about yourself sleep well, eat well exercise

Remote working best practices?
- Dedicate space for work
- Dress for a working day
- Use tools to keep focused
- Good internet, equipment etc.

## Communication

- Everything we do is a form of communication
- Delivery is extremely important, they way we say things can be more important than what you say
- It's a two way street

### If you have poor communication within a business:

- Loss of potential business
- Mistakes
- Lack of coordination
- Damage to corporate image
- Employee frustration
- Poor morale

### What are the barriers to good communication:

- Personal
- Physical
- Geographical
- Cultural
- Organisational

### How to deal with poor communication?

- Don't stereotype
- Be open to ideas outside of your existing beliefs.
- Stay level-headed and treat people with respect
- It isn't personal, they way people act in pressured envrionments isn't often a true representation of themselves.
- Create an environment that thrives on Reciprocity

## Biases

Biases are one of the key ways we can communicate with others

### Anchoring bias

- Relies too heavily on the first piece of information received e.g. someone told you something about someone else
and you anchor to that and assume that for a fact

### Choice-Supportive bias

- The tendency to retroactively ascribe positive attributes to an option one has selected and/or to demote the forgone
 options. It is part of cognitive science, and is a distinct cognitive bias that occurs once a decision is made.

### Confirmation bias

- The tendency to search for, interpret, favor, and recall information in a way that confirms or supports one's prior
beliefs or values.

### Bandwagon bias

- The tendency people have to adopt a certain behavior, style, or attitude simply because everyone else is doing it.

#### There were other biases covered


### Exploiting bias in the workplace

- Reactance - by telling people they are able to say no will make them more likely to say yes.
- Reciprocity - be the first to give the feeling of obligation to give when you receive. Personalised and unexpected makes it even
better.
- Door in the face - Forcing people to refuse a large request increases the likelihood of agreeing to a second smaller request.
- Likeability - give compliments and build cooperation. Freely give honest flattery.
- Social proof - people look to others to determine their own actions

### Hats

- White hat - calls for inbformation known or needed
- Yellow hat - symbolises brightness and optimism
- Black hat - judgement, spot the difficulties and dangers where things might go wrong.
- Red hat - signifies feelings, hunches and intuition. Can express emotions and feelings and share fears, likes, dislikes etc.
- Green hat - Creativity, possibilites alternatives and new ideas, an opportunity to express new concepts and perceptions
- Blue hat - Manage thinking process, its the control mechanism that ensures all hats work

### Dealing with conflict Pt. 2

####Causes of conflict:
- Stubborn
- Disagreements about how to solve a problem/proceed
- Breakdown in communication
- More than one person trying to lead the group
- Having conflicting opinions
- People wont take criticisms/feedback

#### How to deal with conflict:

- Take time to understand the situation - listen to their point of view before reacting and dont respond hastily.
- Know your audience - are they a 'know it all' or are 'close-minded'
- Ask others for their perspective - gain viewpoints from outside of the bubble
- Compromise - find a resolution to satisfy both parties if you can, its fine to capitulate.

Other tips:

- Stay calm
- Adjust body language

