# Project Metrics

We've identified several areas of each project that we feel are
important to the overall health of the project. They're a mix of
technical, client engagement and financial factors that each contribute
differently.

## Client Engagement

* Weekly Engagement

  Planning meetings are important to keep the flow of new work moving.
  We need to talk through new feature ideas, review wireframes, write
  user stories and prioritize them. This happens once a week with the
  Guide, Designer and Product Owner.

  KPI: Weekly Attendance (percentage of planning meetings attended)

* Daily Engagement

  Daily standups are very important to us, and we expect the product
  owner to be involved as often as possible. We always want to be
  building the right thing at the right time, so we need to discuss
  functionality and expectations often.

  KPI: Daily Attendance (percentage of standups attended)

* Happiness

  This one is fuzzy, but just as important. We want our clients to be
  happy with the work we're delivering and the only real way to find out
  is to ask! We ask for a happiness level between 1 and 10.

  KPI: Happiness level (1 - 10)

## Technical

* CodeClimate

  CodeClimate is a service we use to automatically check the codebase
  for things like duplication, complexity and security vulnerabilities.
  The result is a "GPA" which consists of grades across many files
  within the application. The trend of the GPA is a good indicator of
  how the code quality is improving or declining.

  KPI: CodeClimate GPA (0.0 - 4.0)

* Build Status

  Tests are important to us, and automated testing is a good way to ensure
  the project is technically sound and that all the pieces are working
  properly. We're fans of Test Driven Development, so we begin new
  features with tests to prove that the functionality doesn't exist.

  Running the automated tests after each push to the codebase helps us
  make sure we haven't broken existing functionality. Currently, we use
  [Semaphore][semaphore] to run automated tests.
  
  KPI: Build Status (pass/fail)

## Financial

* Receivables

  Good clients pay us on time. We deliver functionality in a timely
  manner and we expect our clients to reciprocate. It's respectful and
  courteous and it's important to our team as well.

  KPI: Time to pay (Invoice Date - Paid Date)

* Weekly Rate

  We're building a business, so meeting our own goals is important. We
  want to ensure that the weekly rate reflects the value we're
  delivering to clients as well as the balance of our own internal
  projects.

  KPI: Weekly rate (% of goal)



[semaphore]: http://semaphore.com
