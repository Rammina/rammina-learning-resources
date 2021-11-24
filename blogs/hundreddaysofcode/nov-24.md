Hello there, everyone!

I was finally able to solve the bug I was stuck on for 2 days.

`Access to XMLHttpRequest at API_GATEWAY_ENDPOINT from origin http://localhost:3000 has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource `

What I did was limit the allowed methods for my API Gateway HTTP API to just POST and OPTIONS methods. I also made sure that the preflight OPTIONS request did not interact with my Lambda function, and only the POST request containing the form data does. Finally, I manually set the access-control headers instead of letting AWS handle it for me automatically, and I was able to fix the issue.

Anyway, let's move on to my daily report!

## Yesterday

I was stuck on this bug:

`Access to XMLHttpRequest at API_GATEWAY_ENDPOINT from origin http://localhost:3000 has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource `

I learned a lot from reading multiple whitepapers about AWS API Gateway, Lambda, and SES.

## Today

Here are the things I learned and worked on today:

### Company Website

- I managed to solve the bug above.
- added validation for my contact form.
- display success message if the message goes through and an error notification if it fails.
- changed the color scheme for my navigation bar.
- added a close button for my navmenu.

### Scrum

- learn the key differences between Scrum and Kanban.
- read a blog post about Scrum and how it uses be principles of Empiricism.
- I did some practice flashcards for Scrum.
- reviewed some of the things I've learned before.

Thank you for reading!

![Thank You Banner](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x9ayfxxxaz2g2hfcqbsk.png)

### Resources/Recommended Readings

- [Agile is constant change](https://www.scrum.org/resources/blog/agile-constant-change)
- [Scrum Master learning pathway | Scrum.org](https://www.scrum.org/pathway/scrum-master)
- [The 2020 Scrum Guide](https://scrumguides.org/scrum-guide.html)
- [Mikhail Lapshin's Scrum Quizzes](https://mlapshin.com/index.php/scrum-quizzes/)

### DISCLAIMER

**This is not a guide**, it is just me sharing my experiences and learnings. This post only expresses my thoughts and opinions (based on my limited knowledge) and is in no way a substitute for actual references. If I ever make a mistake or if you disagree, I would appreciate corrections in the comments!

<hr />

### Other Media

Feel free to reach out to me in other media!

<span><a target="_blank" href="https://twitter.com/RamminaR"><img src="https://res.cloudinary.com/rammina/image/upload/v1636792959/twitter-logo_laoyfu_pdbagm.png" alt="Twitter logo" width="128" height="50"/></a></span>

<span><a target="_blank" href="https://github.com/Rammina"><img src="https://res.cloudinary.com/rammina/image/upload/v1636795051/GitHub-Emblem2_epcp8r.png" alt="Github logo" width="128" height="50"/></a></span>
