# Company Questions

Question to ask companies during the interview process. These questions have no perfect solutions.

Good companies will be able to cite the "breadth" of these solutions. Great companies will provide details into subtleties (depth) of some of those solutions.

Branch this doc for each company you interview with and put answers inline.

TODO: Add rubrics for scoring

## Engineering Culture

Changes in external dependencies often cause or expose bugs in code -- both your own and others. See [Hyrum's Law](https://www.hyrumslaw.com/). A change in your software has the potential to break users. Updating system packages can often implicitly break your own application.

_Question_: How does your company deal with this?

_Solutions_:

- Monorepo ensures all tests can be run when dependencies change.
  - Running every test on every code change in a monorepo is non-sustainable
- Integration testing
  - More maintenance required. Often fails to capture new failure modes
- Multiple maintained branches with different amounts of customer "soak" times. (e.g. linux LTS releases)
  - Multiple branches require extra maintainers for backports
- VM images/containers to minimal set of trackable dependencies
  - Only catches issues occurring late in the dev testing cycle
- [Hermetic](https://bazel.build/basics/hermeticity) builds
  - True hermetic builds are typically impossible. libc is typically a required DLL
  - Compilers and build infra used in builds also introduce non-hermeticity

## People Culture

### No Jerks

[Jerks](https://en.wikipedia.org/wiki/The_No_Asshole_Rule) co-workers cause unnecessary attrition and issues in project execution.

_Question_: What methods do you use to filter these out?

_Solutions_:

- Behavioral interview questions
  - Studies [suggests](https://pmc.ncbi.nlm.nih.gov/articles/PMC4856718/) that the reason for their efficacy is that it selects for individuals "Knowing How You Should Behave" rather than "How You Would Behave"
  - What do you look for in answers to filter out jerks?
- HR Intervention
  - HR often only intervenes for gross violations
- "Managing out" bad employees
  - Relies on managers themselves not being jerks
- Peer feedback
  - Fear of retribution
  - Potential solution: stack-rank jerks

### Exit Interviews

Giving negative feedback can only have negative consequences on working relationships. The only time you can elicit honest feedback is when an employee leave a company. This is true for both an attritioning employee giving feedback about management; and for other employees giving feedback on an attritioning employee.

Most companies don't do exit-interviews for legal [reasons](https://www.law.com/thelegalintelligencer/2019/04/29/exit-interviews-do-the-benefits-outweigh-the-risks/?slreturn=20250806172058). Thus a company that chooses to perform exit-interviews makes a conscious decision to trade honest feedback for legal liabilities.

_Question_: Does your company do exit interview?

_Solutions_:

- Yes
  - What kind of questions do you ask during these interviews? How does that feedback and incorporated back into the company?
- No
  - What other methods do you use to ensure that employees are not leaving because of toxic management?

## Management Culture

_Question_ (_Large companies_): What is your company's mission statement and/or its core values? Either implicit or explicit.

_Solutions_:

- Yes
  - Follow up: Can you give an example of how management employed these values in the past?
- No
  - How else does the leadership ensure a consistent vision?

**Alternatively** (_Medium companies_): Does your company do Townhalls/Q&As? Why or why not?

_Solutions_:

- Yes
  - Follow up: Can you give an example of an Q&A that resulted in an action taken by management.
- No
  - Follow up: How does the company ensure ICs have input in executive decision-making?

**Alternative** (_Small companies_): Under what scenarios would you quit the company?

_Solutions_:

- Company gets bought.
  - Under what conditions would you stay with the company even if it were bought? See if people know why they are working here.
- Company does something unethical
  - What kind of ethical breaches would qualify? See if people working here have personal ethics.

## Technical Execution

_Question_: "Does your org use agile practices? Which ones and why?"

_Solutions_:

- No
  - If not, what do you do instead to make sure programs execute on time?
- Yes
  - The subtlety is if leadership has a good understanding why they've chosen the practices they have or if teams have the agency to choose which ones to use.
  - e.g. why do planning poker if you aren't shipping a product by a deadline?

## Management Practices

### Promotion

_Question_: What is the goal in promoting someone?

_Solutions_:

- To pay them more
  - Why not just give out a bigger bonus
- Recognition
  - Does this not just encourage ladder-climbers
- To reinforce a meritocracy. People who make good decisions should be making important decisions.
  - Hierchies can stifle innovation since it cuts out juniors from decision-making
  - What metrics are used to determine who is better at decision-making?

### Key Performance Indicators

_Question_: "Does your org use KPI practices? For what purpose?"

_Solutions_:

- Management Tool. Used to ensure managers are doing what they are supposed to do.
  - Does this extend to ICs then? How do you ensure KPIs don't get gamed?
- Promotion.
  - How do you determine what KPIs are worthy of promotion?
- No KPIs
  - How do you ensure managers do what they are supposed to do in a way that HR and promo committees can recognize?
