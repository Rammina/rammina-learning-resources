Good day, everyone!

Today was my weekly visit to the physical therapist, so I wasn't able to code much.

I didn't really make that much progress because I was still stuck on the same problem as I was yesterday. I spent most of the time troubleshooting my AWS API Gateway integration and Lambda function. Apparently, there is something wrong with the preflight request part of the communication between frontend and backend. I used tools such as AWS CloudWatch Logs to retrieve the error message for the integration of the API Gateway.

I'm hoping that I manage to solve this issue tomorrow.

Anyway, let's move on to my daily report!

## Yesterday

I set up my contact form to connect with the AWS serverless backend, but I got stuck on this bug:

```Access to XMLHttpRequest at API_GATEWAY_ENDPOINT from origin http://localhost:3000 has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource.

```

I also selected a design scheme for my website.

## Today

Here are the things I learned and worked on today:

### Company Website

- I spent most of my time trying to solve the bug above.
- reviewed how to use CloudWatch Logs to gain insight as to what's going on with the AWS services I use.
- learned a lot about CORS.
- did a lot of searching about Access Control headers.

### Scrum

- I learned about why the Daily Scrum is more than just a status report.
- I did some practice flashcards for Scrum.
- reviewed some of the things I've learned before.

Thank you for reading!

![Thank You Banner](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x9ayfxxxaz2g2hfcqbsk.png)

### Resources/Recommended Readings

- [Using AWS Lambda with Amazon API Gateway](https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html)
- [Troubleshooting issues with HTTP API Lambda integrations](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-troubleshooting-lambda.html)
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
