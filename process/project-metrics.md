# Project Metrics

We've identified several areas of each project that we feel are
important to the overall health of the project. They're a mix of
technical, client engagement and financial factors that each contribute
differently.

## Client Engagement

This is really cool

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

  [CodeClimate][codeclimate] is a service we use to automatically check
  the codebase for things like duplication, complexity and security
  vulnerabilities.  The result is a "GPA" which consists of grades
  across many files within the application. The trend of the GPA is a
  good indicator of how the code quality is improving or declining.

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

* Work in Progress

  Too many things happening at once can lead to all of them being
  implemented poorly. Our focus should be deliberate on one feature at a
  time as often as possible.

  > "You have to make every single detail perfect. And you have to limit
  > the number of details."
  > <br />-- <cite>Jack Dorsey, founder of Twitter and Square</cite>

* Cycle Time

  Cycle time is defined as work in progress divided by the average
  completion rate. The cycle time clock starts when work begins on the
  request and ends when the item is ready for delivery.

  > Cycle Time = WIP / Average Completion Rate

* Throughput

  Throughput is the number of things that can be done in a given amount
  of time. It's calculated by dividing work in progress by cycle time.

  > Throughput = WIP/Cycle Time

  Since throughput relies on actual start and finish times we can derive
  a predictive measure for forecasting without any estimating. This is
  important to us because the past becomes an excellent predictor of the
  future.

* Lead Time

  Lead time is the time it takes for a new card to go from planned to
  delivered and in production. It's important to us because we always
  want that time to decrease. We want to get better at delivery of
  features as soon as we possibly can.

You can read more about work in progress, cycle time, throughput and
lead time here:

  * [Wayne Allen's Blog][wallen]
  * [Stefan Roock's Blog][lead and cycle]
  * [AvailAgility][availagility]

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

[codeclimate]: http://codeclimate.com
[semaphore]: http://semaphore.com
[wallen]:
http://weblogs.asp.net/wallen/archive/2008/10/23/throughput-vs-velocity.aspx
[lead and cycle]:
http://stefanroock.wordpress.com/2010/03/02/kanban-definition-of-lead-time-and-cycle-time/
[availagility]:
http://availagility.co.uk/2008/10/28/kanban-flow-and-cadence/
