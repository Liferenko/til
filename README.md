# TIL (Today I Learned) 
inspired by [jbranchaud/til](https://github.com/jbranchaud/til?tab=readme-ov-file)


**around-tech:**
- [Comfy life](comfy_life/)
- [Fundrising](fundrising/)
- [Interviews](interviews/)

**Tech:**
- [Elixir](elixir/)
- [Erlang](erlang/)
- [Vim](vim/)
- [Unix](unix/)














---
##### Unsorted yet

Rob's boost (aka course) - https://skilstak.io/boost/start/




## 2024-05-15 08:14

how Design patterns look in Elixir: 

1) Mediator
    Examples: Phoenix Controller, Phx LiveView
    Solutions:
    - Funcs and modules for controlling and coordinating logic
    - Processes for controlling and coordinating events

2) Facade
    Examples: Phx Contexts, Logger, Elixir compiler
    Solutions: Modules prociding a simplified API to the more general facilities of a subsystem

3) Strategy
    Examples: 
    Solutions:
    - Pattenr matching
    - Anon functions
    - Interfaces from OO a.k.a Protocols in Elixir
    -- interfaces are a mechanism for polymorphism (with upfront contract)"(c) José Valim
    Polymorphism in Elixir:
        Behaviour == Modules
        State == Data
        Mutability == Processes

    "Favor object composition over class inheritance"(c) Gang of Four

Source: https://www.youtube.com/watch?v=agkXUp0hCW8






















## 2024-05-14 06:07

testcontainers (Elixir friendly) - https://testcontainers.com/desktop/?utm_campaign=2024-04-24-testcontainers-desktop&utm_medium=video&utm_source=youtube




## 2024-05-09 12:00

Peer code review - https://smartbear.com/learn/code-review/best-practices-for-peer-code-review/



Interview intro
# v2:
## Intro + ice breaker
:) I suck in JS
:) “normal” job before SWE
:) audio-device’s driver has been installed incorrectly

- 7 years of exp in production. 4.5 years in PETAL  stack (day-to-day)
- before IT I used to have a “normal” job in marketing.
Marketing -> automation the Adv processes (Google Ad, Facebook Ad etc, analytics) -> full-time software engineer

## the latest project
- Zoom-like, Miro-like platform.
solution !exactly! for education
for teachers, tutors

BE - audio, video calls, recording, speech recognition
FE - upgrading whiteboard. Admin pages
Infra - docker configs, log management, GH Actions for auto tests

#### Most challenging moment:
S - new team, new stack, 99% homebrewed tools
T - join the process ASAP
A - ask-ask-ask
R -  



#### Fuck-up moment:
S - I suck in JS. 

## questions?


























































## 2024-05-06 10:34

Summary of Clean Code - https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29

Yet another intrepretation of my rule is a Boy scout rule: Leave the campground cleaner than you found it.



## 2024-05-03 18:25

:queue.* is awesome in Elixir




## 2024-05-02 11:34
Dockerfiles, .sh files, Makefiles can wrapped in Earthfile here - https://docs.earthly.dev/basics/part-1-a-simple-earthfile




## 2024-05-02 07:38
Erlang doc based on Hexdocs - https://erlang.org/documentation/doc-15.0-rc3/lib/stdlib-6.0/doc/html/rand.html




## 2024-05-01 19:16
Zen of Erlang - https://ferd.ca/the-zen-of-erlang.html




## 2024-04-30 10:00
Get a feedback from Roman that's we won't work together. :/ Sad but ok

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% Above is moved in TIL %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


## 2024-04-25 12:49

Git commit messages Policy - https://www.conventionalcommits.org/en/v1.0.0-beta.2/#:~:text=Commits%20MUST%20be%20prefixed%20with,bug%20fix%20for%20your%20application.




## 2024-04-25 05:57

for using doctest without import issue, I need to use `doctest SomeLongModuleName.SubModule, import: true`



## 2024-04-25 05:05

Github scanner for HRs and pre-interview screening - https://gitroll.io
Works meh, but it might be a ice breaker




## 2024-04-16 15:00

Erlang VM registers all nodes. I may call `epmd -names` to see all my nodes




## 2024-04-16 14:46

Find related subreddits by a keyword
`https://anvaka.github.io/sayit/?query=tutor`




## 2024-04-05 16:25

List of all Membrane Plugins here - https://github.com/membraneframework/membrane_core/#All-packages




## 2024-04-05 07:54

Performance, profiling and all-about-the-project info for Elixir projects
https://gitlab.com/MachinesAreUs/archeometer

works unstable for existing project, but maybe I need to spend more time with it




## 2024-03-25 17:34
Devtools console shows IEx console logs - 

```
 # config/dev
  config :my_app, MyAppWeb.Endpoint,
    live_reload: [
      interval: 1000,
      patterns: [...],
+     web_console_logger: true
    ]

 # app.js
 + window.addEventListener("phx:live_reload:attached", ({detail: reloader}) => {
+   // enable server log streaming to client.
+   // disable with reloader.disableServerLogs()
+   reloader.enableServerLogs()
+ })
```

https://www.elixirstreams.com/tips/stream_server_logs_to_console?utm_source=elixir-streams-newsletter



## 2024-03-11 18:21




## 2024-03-09 09:04

"The life the law has not been logic: it has been experience."(c)
    Oliver Wendell Holmes, Jr. in his book, The Common Law, said




## 2024-03-08 10:58
When preparing your file to send to an Estonian court, you should follow specific guidelines to ensure its correctness and acceptance. Here is a summary of the key points based on the provided text:

1. **Language**: All documents, including the complaint, must be in Estonian. If the person seeking legal action does not speak Estonian well, they can request translation assistance.
2. **Format**: The complaint should be submitted electronically through the e-toimik system, via email to the designated court email address, or in A4-sized paper with clear and legible printing.
3. **Content of Complaint (Hagiavaldus)**: The complaint should include the following information:
    - The court to which the complaint is addressed.
    - Personal details of the plaintiff (hageja) and defendant (kostja), including names, personal codes or birth dates, addresses, and contact information.
    - Clearly stated claim or demand (nõue) of the plaintiff.
    - Factual basis (hagi alus) supporting the claim, including relevant details.
    - Evidence (tõendid) supporting the factual basis, specifying the type of evidence.
    - Claimed amount (hagihind) if the complaint is not directed towards a specific sum of money.
    - Whether the plaintiff agrees to resolve the matter in written proceedings or wishes a court hearing.
    - Whether the plaintiff requires a translator's assistance.
4. **Signatures**: The complaint must be signed. If the complainant is represented by someone other than an attorney, a power of attorney (volikiri) must be attached.
5. **Fees**: A state fee (riigilõiv) is applicable, and it depends on the claimed amount in the complaint. Some cases may be exempt from state fees. If the complainant cannot afford the fee, they can request legal aid for fee payment.
6. **Additional Notes**:
    - Ensure all documents are in the Estonian language or accompanied by an Estonian translation.
    - Follow the jurisdiction rules when selecting the court based on the defendant's residence or the location of a legal entity.

Remember, this is a brief summary, and you should refer to the specific legal provisions in the Civil Procedure Code (Tsiviilkohtumenetluse seadustik) for detailed and accurate information. Always check the latest legal requirements and guidelines from authoritative sources or consult legal professionals for specific cases.



---
## version 0.1
Translate it in Eesti
Request a translation assistance

!!!!!!!!!!!!! В административном производстве должны быть указаны имя, адрес (в т. ч. эл. почта), личный код или дата рождения подателя жалобы, данные ответчика, содержание жалобы и подпись подателя жалобы.

    ### The court to which the complaint is addressed.
    Tallinn Administrative Court

    ### Personal details of the plaintiff (hageja) and defendant (kostja), including names, personal codes or birth dates, addresses, and contact information.
    Plaintiff: Individual Entrepreneur Pavel Liferenko, Registration ID 305461568, Tax payer ID 305461568 Adress: Georgia, Tbilisi, Saburtalo District, Gamsakhurdia Avenue, near N34. Email: liferenko.it@gmail.com
    Defendant: Introduct Estonia OÜ, a company duly incorporated in Estonia under Reg.No.14037952, VAT No. EE101887614, address: Pärnu mnt 16 Tallinn Harjumaa 10141, Estonia, represented by the Director Viktor Larionov, acting under the Statute of the company. Email: enquiry.estonia@introduct.tech

    - Clearly stated claim or demand (nõue) of the plaintiff.
    The company Introduct Estonia OÜ  declined to send a paycheck for a period since 01.01.2024 to 16.01.2024, uniletirally terminated a contract with contract violation, refused to provide the data confirming a notifications of the decision to refuse payment for January 2024. 






        10.1. This Contract shall enter into force upon the date of signature and is valid until September 11, 2024. 10.2. This Contract shall terminate:
        10.2.1. upon the expiration of its term;
        10.2.2. ahead of time by mutual consent of the Parties.
        10.2.3. ahead of schedule unilaterally:
        10.2.3.1. on the initiative of the Customer, with a written notice of the Contractor not less than 14 days before the termination of the Contract;
        10.2.3.2. on the initiative of the Customer, without prior notice, in different ways, as Contractor systematically allows blocking and/or critical mistakes (two or more times) and/or moderate minor mistakes (more than 10 times during the reporting period) and does not eliminate such shortcomings in the terms determined by the Customer, or stopped providing services at all without any reason and did not to notify the Customer;
        10.2.3.3. on the initiative of the Contractor, with written notice to the Customer not less than 14 calendar days before the termination of the Contract.


    - Factual basis (hagi alus) supporting the claim, including relevant details.
    TODO 3) uniletirally terminated a contract with (contract violation)
        according to 10.2.3.2 I haven't been notified about critical mistakes and/or moderate minor mistakes, haven't been notified about the terms determined by the Customer, have not stopped providing services at all without any reason until January 16th 2024.

    1) 19.02.2024 I sent an email with a request when a paycheck for January will be sent (usually, it's between 10th and 16th day of next month). 
    2) Introduct Estonia OÜ did not notified about final decision and looks like they planned to not send any email if I didn't send them an email to clarify the payment situation.
    At January 16th, 2024 HR director wrote that payment will be in next month (as usual) but month later the company changed it's mind. Which means the company terminated a contract without preparation and calculation. 

    3) Last work day - Tuesday, 16.01.2024. Exit interview with HRD - Sunday, 14.01.2024  (we haven't ever have any meetings at weekends). Email has been sent 2 days after exit interview (screenshot #11090109)

    - Evidence supporting the factual basis, specifying the type of evidence.
    4.2.1. To provide the Contractor with the information required to perform the services determined in TA.
    4.2.2. To accept the results of the services of proper quality provided by the Contractor by signing the Act of Acceptance.
    The company refused to pay based their arguments on a state 4.2.2 of the contract.
    For a period since 12-09-2022 to 16-01-2024 none of acts of acceptance have been signed between me (Contractor) and the company (Customer). But the company were paying paycheck without any additional documents. Each month I as the Contractor was receiving 2 documents: an invoice and a specification. Source of communication: cloud-based team communication platform named Slack with Introduct's corporate account.

    Компания отказывается оплатить оказанные услуги за период январь 2024, ссылаясь на отсуствие подписанного акта приёмки выполненных работ. Судя из этого утверждения, в период с сентября 2022 по декабрь 2023 компания оплачивала услуги только с подписанным актом приёмки выполненных работ и сможет предостабить данные документы с подписями обеих сторон. Я в период с сентября 2022 по декабрь 2023 упомянутые документы не получал и не подписывал. Получал 2 вида документа - invoice и specification за конкретный период.
    Отсюда вытекает, что компания имеет практику оплаты оказанных услуг без акта приёма выполненных работ.
    11 марта 2024 я запросил у Introduct HRD для ознакомления подписанные акты приёма выполненных работ за период октябрь 2023, ноябрь 2023 и декабрь 2023 
    (screenshot #100193283)

    If the company meant the act of acceptance between Introduct Estonia OÜ and client company, it means that for the period from 01-01-2024 to 16-01-2024 the company didn't accept the Contractor's work and shall not receive a payment for the work done by Contractor. But the fact "the company holds Contractor's paycheck to cover education expences" meant that the company accepted the Contractor's work and received Contractor's paycheck by client company.

    Quote "during the final calculation, the financial department raised the history of cooperation with the company and according to history, you began cooperation as part of your training and a few months later began activities with a commercial project. The January amount was counted as tuition reimbursement and will not be paid."
    (screenshot #11090122)
    Our contract does not contains statutes about tuition,
    3300 usd per month during training period (document #313001)
    3800 usd per month after training period (document #9929483)

    4.2.3. To perform the payment to the Contractor for the provision of the services according to the section 3 of
    the Contract.

    - Claimed amount (hagihind) if the complaint is not directed towards a specific sum of money.
    Remunement for January 2024 + % delay fee 12.5% per year + expences for court services

    - Whether the plaintiff agrees to resolve the matter in written proceedings or wishes a court hearing.
    I agree to resolve the matter in written proceedings

    - Whether the plaintiff requires a translator's assistance.
    Yes, I request a translator's assistance



























































## 2024-03-05 19:39
Law English dictionary:
1) https://www.nolo.com/dictionary
2) https://thelawdictionary.org/letter/m/



## 2024-02-26 11:47

ETS tables are never garbage collected. Only removing records manually will reclaim memory
Don't use dynamic atoms. They are cached till VM running

Erlang/Elixir debugging - Tracing here - https://www.youtube.com/watch?v=pj6zAgvVt5w - Timestamp 21:00




## 2024-02-26 10:24

how to resolve ssh issue for new ubuntu machine (usually for home-based servers )
https://locall.host/why-cant-i-ssh-into-ubuntu/
















## 2024-02-25 13:17
Legally, the advertisements are not offers. Instead, they are held to be invitations for you to come and make an offer.

Now the big thing about revocation is that you have to do it before it's accepted
The third method by which offers will be terminated is called operation of law. Things like the death or incompetence of one of the parties, destructing of subject matter, or an unreasonable lapse of time

### Acceptance
Rejection is easy: just say no. But for acceptance there are a few requirements in order to have a valid acceptance of an offer and form a valid and enforceable contract.






















## 2024-02-24 20:15
in contract there always at least 2 parties
offeror
offeree

valid contract
void contract



## 2024-02-23 22:09

today I learned how to experiment with Ansible via Docker
https://medium.com/@mefengl/unknown-title-a4d9400b7bf0

useful when I need to dry-run and test some playbooks without setting any VMware or VBox (useful for mac M1)



## 2024-02-19 17:02

Nice explanation of OTP basic concepts - https://www.youtube.com/watch?v=ENolm5T0bkU&list=TLPQMTkwMjIwMjSk3L8IdXWFtQ&index=5




## 2024-02-14 09:34

Rust for 



## 2024-02-13 18:30

I can use `Process.send_after/2` 
send_after(dest, msg, time, opts \\ [])
Sends msg to dest after time milliseconds.

use it istead of cron jobs.

And I may use gen_retry for retriving -  
https://github.com/appcues/gen_retry

---
Find begginer-friendly post about Rust and Arduino. I may try it
https://blog.logrocket.com/complete-guide-running-rust-arduino/



## 2024-02-12 15:58

# Write a short program that prints each number from 1 to 100 on a new line.
# 
# For each multiple of 3, print "Fizz" instead of the number.
# 
# For each multiple of 5, print "Buzz" instead of the number.
# 
# For numbers which are multiples of both 3 and 5, print "FizzBuzz" instead of the number.

















































































## 2024-02-02 15:45

read carefully this - deps/phoenix_live_view/lib/phoenix_live_view.ex 




## 2024-02-01 11:36

- Strong arrows in Elixir
```
$ int() -> boolean()
def active?(state) do
    if state > something do
        true
    else:
        false
    end
end
```

same way usually I used it like this:
```
def active?(state) when is_integer(state) do
...
```

Source - https://elixir-lang.org/blog/2023/09/20/strong-arrows-gradual-typing/




## 2024-01-29 11:11

Phoenix has an awesome module - Naming
`Phoenix.Naming.camelize/1` - convert "any_like_that" into "AnyLikeThat".
Or it might be useful here 
`Phoenix.Naming.humanize(:created_at)` -> "Created at"

https://hexdocs.pm/phoenix/Phoenix.Naming.html




## 2024-01-24 18:50

pull-up resistors
pull-down resistors









































## 2024-01-20 10:04

if use `"+y` with selected text in Vim - you yank it in a clipboard. 
WHAAAAT?:)




## 2024-01-15 14:08

My forecast after tough performance review:
- Client relationship ends. I excluded from all chats + excluded from Github repo (nope, Im still in Github and in daily meeting)
- Outsource company's HR will start shitty chat.
- Varieria will start aggresive speech with Pasha name. 
- Outsource company won't fire me because Im money source
- Im on a bench
- I think 1-2 months with Client after shitty review

Result at the start of the day: none of forecasted points have been true
Result of mid-day
Result at the end of the day





































## 2023-12-14 14:45
String.to_atom/1 is a danger

```
String. to_atom creates a new atom if one of its name wasn't use before, which is dangerous for dynamic/unknown data. String. to_existing_atom does only allow you to convert strings to atoms when the atom already exists at that point via some other means of usage of it.
```

according to it - 
https://www.erlang.org/doc/efficiency_guide/introduction
https://hexdocs.pm/credo/Credo.Check.Warning.UnsafeToAtom.html



## 2023-12-11 14:02
how to get a port owner PID & kill thy process
`kill -9 $(lsof -t -i :5432) ; docker compose up -d`




## 2023-12-04 12:46
Book OTP guide book




## 2023-12-04 06:53




## 2023-12-03 11:10


---
before Notes have been created - I used this "100daysOfSRE"
2023-11-12

When I will be on an interview again - I'd like to ask what tools company's team use in communication.
Teams & Outlook - red flag
Slack - hmm, well-enough
Discord - means the team is friendly and nerdy enough to use the best known tools


---
2023-11-09

# Error:
:observer.start() is not starting in IEx 

### Solution:
You can do extra_applications:

---

```
if Mix.env == :dev, do: [:observer, :wx, :logger, :runtime_tools], else: [:logger, :runtime_tools]
```










2023-09-29
1) An alternative to `with` usage in Elixir - https://hexdocs.pm/sage/readme.html
`It’s like Ecto.Multi but across business logic and third-party APIs.`

instead of 
```
  with {:ok, user} <- create_user(attrs),
           {:ok, plans} <- fetch_subscription_plans(attrs),
           {:ok, charge} <- charge_card(user, subscription),
           {:ok, subscription} <- create_subscription(user, plan, attrs),
           {:ok, _delivery} <- schedule_delivery(user, subscription, attrs),
           {:ok, _receipt} <- send_email_receipt(user, subscription, attrs),
           {:ok, user} <- update_user(user, %{subscription: subscription}) do
```

we may use this:
```
 new()
    |> run(:user, &create_user/2)
    |> run(:plans, &fetch_subscription_plans/2, &subscription_plans_circuit_breaker/3)
    |> run(:subscription, &create_subscription/2, &delete_subscription/3)
    |> run_async(:delivery, &schedule_delivery/2, &delete_delivery_from_schedule/3)
    |> run_async(:receipt, &send_email_receipt/2, &send_excuse_for_email_receipt/3)
    |> run(:update_user, &set_plan_for_a_user/2)
    |> finally(&acknowledge_job/2)
    |> transaction(SageExample.Repo, attrs)
```
---

2023-09-28
1) looks like I can avoid bash scripts with Terraform Providers or K8s KinD usage (https://kind.sigs.k8s.io/docs/user/working-offline/)

---

2023-09-13
1) kubectl alternative? Hmm, k9s looks interesting

---

2023-09-11
1) kinda ready-to-use ECK configs - https://github.com/framsouza/eck-ready-for-production/blob/main/external-dns.yaml



--- 
2023-07-02
1) `kubectl get pods -A` to check which of your pods are running if you don't know your namespace



---

2023-07-02
1) Bad SQL for removing expired items -
`SELECT ... WHERE DateDiff(mm, OrderDate,GetDate()) >= 30;`
Fixed: `SELECT ... WHERE OrderDate < DateAdd(mm, -30, GetDate());`


---

2023-07-01
1) "The more pressure you take, the more pressure you will get" - once being said in ThePrimeagen video here - https://www.youtube.com/watch?v=3J6ZpoPWauI
So saying "No" will play good game for me right now AND will play better in long run

---

2023-06-24
1) Way better to use language model "Yes and..." instead of "Yes, but" in any type of conversation

---

2023-06-23
1) Algo course notes:
    - ask better clarifying questions
    - writing the code - is the last thing to do and its optional
    - ask questions earlier

    - shape data structure(s) to the problem - not the problem to the data structure
    - the 1st solution you do - should be dummiest and easiest solution that accurate. Optimize it later
2) 

---

2023-06-22
1) did a bit of rm-to-rip typelearning
2) found a Warp (CLI alternative). So far so good. Looks fancy. Works with Tmux

---

2023-06-18
1) A course "Rust for TS developers" is done. The course is good, useful, quite "dry" and cover 2 main concepts: trait+imp+generics and Borrow checker.
I think it's quite good for starting up.
2) `rustup docs --book` - offline Rust book

---

2023-06-17
1) I can't say I got the 100% of generic idea. I got the result it wants to reach: to be 1 for every situations. And that's pretty nice. Kinda macro from Elixir: lets generate all possible variants for every situation.
2) I think I got the idea of `impl<T, U> ...` - it means that 2 types might be different (ex: f64 and i32) BUT in some cases it still will work when T=f64 and U=f64. We cover both cases: when they are same and they are different. With `impl<T>` we won't have this opportunity to cover both.

---

2023-06-16
1) `cargo install cargo-watch` + watch only `/src` and clear the console - `cargo watch -c -w src -x run`
2) done with yesterday's code where From and IntoIter had been kicked my brain out.
Now Dispay works, Iter works for Rectangle, `collide/2` works (but I'm not sure it works okay for Rect-within-Circle cases)
3) how to public rust app in brew - https://federicoterzi.com/blog/how-to-publish-your-rust-project-on-homebrew/


---

2023-06-15
1) Display and Default. Boom! Looks good, I hope I will use this knowledge :)
2) vim knowledge boom moment: I saw how ThePrimeagen did "add lost brackets to the end of the line for this N lines". It works this way: select the lines, press shift+:, it shows `:'<'>` and here I can use any of commands. For this example it was :s/%pattern_to_change%$/%new_pattern/g.
Dollar sign is the sign "The end of the line"

---

2023-06-13
1) added Rust-written music player. Vim keybindings, shitty look.. oh, thats what I was looking for :)
2) played around Rust tutor this time. Modules + crates + `use ...` - goes okay. Lovin' it

---

2023-06-10
1) vec![...] is temporary. We need to declare it in a var and use it AFTER - now the vec! will be in a memory
2) kinda worked out with structs, impls and triats. Structs were useing for objects (Circle, Rectangle), impl for their action with specific struct (Area for Circle, Area for Rectangle) and triat for the action we want to do with the all structs (Area)
3) idea of learning project - thinky-type the RIP project (Rust-written rm command)
4) `::std::io::...` use for absolute path. At the same time `std::io::...` is pretty standart

---
2023-06-10
1) if I need to get a String from args but stuck with Option<String> - maybe I need to use .expect("error msg") at the end.
Example
```
    let path: String =
        env::args()
        .last()
        .expect("should be at least one arg");
```
2) kinda hard part when I tried `trait` to add it by myself. But resolve it with some hinds from a course
3) `.parse::<T>()` can have `.parse::<T>().ok()` or `.parse::<T>().err()`
4) Rules:
    - there might be only one owner
    - there might be unlimited amount on immutable borrows (references, or my example: read-onlys);
    - there might be only one mutable ref (or my example - RWs) and no immutable refs

---
2023-06-9
1) watched a little :/ it was moving-out day

---
2023-06-8
1) worked with Option, .get(index) and *num, &num and *&num

---
2023-06-7
1) Played around .collect() and .iter()
2) Coc-rust works kinda good for Nvim with rust. Nice!
3) worked pretty ok with tutorial this night

---
2023-06-4
1) NOW I can say pattern matching is working in Rust pretty the same way it works in Elixir and Erlang
2) for using any sign as an alias name in ZSH - I need to add backslash. Example: \? 
3) question_mark now works quite okay. The goal of this app is reached. Nice! 

4) in Rust we may use `let y = &x` as a read-only reference and `let y = &mut x` as RW reference.
This RW-* is kinda new for me. 
When we need to use `&mut x` - we must declare `x` as mutable - `let mut x = ...`

in Rust docs it says:
```
    let mut x = vec![1, 2, 3];
    let y = &mut x; // y is a mutable reference to x
```

In this example, y is a mutable reference to the vector x. The reference y can be used to modify the vector's elements without transferring ownership.

---
2023-06-3
1) bought a course "Rust for TS devs". Start!

---
2023-06-2
1) Tried amazing thing: idea -> chat.openai -> CLI app in 25 minutes

---
2023-06-1
1) tried to compile rs-file without main function. For now I'm not sure I know how to do it :)
2) a scope in Rust works quite obvious. I like it: {} define the scope.
3) Rust's compiler can teach me. Nice!

---



---
before Notes have been created - I used this "100daysOfRust"

2023-04-12
1) :AI in nvim works and works pretty awesome
2) :DBUI solves my tasks and works pretty awesome as well

---

2023-04-06
1) how to compile ex project with maximum check of errors and warnings
`mix compile --all-warnings --warnings-as-errors`

---

2023-04-04
1) pgcli connection to remote db
`pgcli postgresql://user:password@host:port/dbname`
---

2023-03-29
1) found OpenCommit here - https://github.com/di-sukharev/opencommit
it helps with commit messages

2023-03-21
1) `curl http://169.254.169.254/latest/meta-data/spot/instance-action` - we need to ask this url constantly
to catch a termination signal
Idea: Elixir or Erlang, make a tiny service to catch this signal 


2023-03-20
1) launched around 10-12 AWS spot instances. Got some insights about. 
Looks like it decrease my AWS costs in April

---------

2023-03-8
1) finally mosh works with AWS. This time it was quite easy to config. 

---------

2023-02-05
1) Weylus - a screen sharing with any device which has browser and same WiFi.
Might be a usecase for a coding inside a vehicle. BT keyboard + phone == laptop-free coding session inside a vehicle
Next step - to try to config it as a second monitor (https://github.com/H-M-H/Weylus)

---------

2023-02-02
1) Playwright - e2e testing better than selenium

---------

2023-01-23
1) git cz makes it easier to git-commit with templates

---------

2023-01-17
1) Need to kill process but donno the pid?
`pidof %app_name`

---------

2023-01-09
1) Too many processes sit on one port? Wanna kill them all? 
`sudo fuser -k %PORT%/tcp`

---------

2023-01-06
1) Now I can make a text-based-screenshot of Tmux pane. Prefix+Alt+P - screenshot

---------

2023-01-04
1) ? as an alias for `w3m google.com` is the power!
2) w3m looks like my choice as well. FInally feels better and way more useful
3) I tried to add dark theme to DBeaver - it killed this app. Thats a bad news. 
4) Good news that I installed gobang - CLI dbeaver app :) Feels nice so far :)

---------

2023-01-01
1) First note in 2023. It turns out Imma a decade developer now. First commit I did was in December, 23th, 2013. Khool

---------

2022-11-21
1) 12V-220V invertor ain't cost bazillion dollars. It costs around 10 usd. Damn! I didn't know that
2) Gmail has a functionality "mark all unread and remove them by one click". I thought I can make it only with partitions (50-100 emails per partition)

---------

2022-11-20
1) one step closer to my Blacklog application for Android. Now it can stop when time's up

----------

2022-11-19
1) Android Studio might work with Android device via WiFi. It's possible to debugging your app here and remotely
2) Vim bindings work quite well in Android Studio
3) My first forked Android app was launched on my Xiami Redmi POCO X3.
4) I defined TODOs for Blacklog

2022-11-08
Today I learned:
1) in Elixir it is possible to String.split nur only with one splitter but with a list of them. Exhibit A: 
String.split(asf, ["/", " ", "+"])

--------------

2022-11-03
Today I learned:
1) ElixirLS and ErlangLS still work bad on my laptop :/ Sucks

--------------

2022-11-02
Today I learned:
1) its better to keep a diary (aka journaling)
2) Nice idea to make (or remake) Elixir projects (nano projects) to Erlang

--------------

2022-10-30

Today I learned:
1) Looks like all I need to use for certification preparations is tutorialdojo. It covers all areas: time-limited quiz + explanations after time is up
2) AWS CloudTrail Log File Verification can detect when log-file was made up (it calls "has been tempered with")

---------------
30 days of AWS started here
---------------


2022-09-15

Today I learned:

1) Erlang trouble with ASDF - the solution was in GCC
source - https://elearning.wsldp.com/pcmagazine/configure-error-no-acceptable-c-compiler-found-in-path/

---------------


2022-09-13

Today I learned:

1) Where to get knowledge about OTP? Here - https://learnyousomeerlang.com/what-is-otp
2) Ansible has an AWS opportunity - https://docs.ansible.com/ansible/latest/collections/amazon/aws/ec2_instance_module.html#examples

---------------


2022-09-4

Today I learned:

1) Redshift is C-store
2) C-store is Columnar storage. Row vs column storage idea looks pretty understandable

---------------


2022-08-31

Today I learned:

1) Summer moved on. Result: my first summer with LeetCode solved tasks
2) SQL tasks looks too easy? Try medium and hard one

---------------


2022-08-30

Today I learned:

1) Erlang/Elixir have BIF and NIF.
BIF - build-in functions
NIF - native inplemented functions. NIF might be used when you need to use Clang in your code.

---------------


2022-08-16

Today I learned:

1) Browser-like search in Tmux - tmux’s default key sequence to enter copy mode and begin a search of the terminal history/scrollback is pretty awkward: Ctrl + b [ Ctrl + r if you’re using the default emacs-style copy mode bindings, or Ctrl + b [ ? if you’re using the vim-style bindings.

---------------


2022-08-13

Today I learned:

1) LeetCode: solved an easy task about tree root and children. It shows out how drastically far Clang goes from Elixir (or vise versa). 
Elixir - ~300ms and ~50mb of RAM for calculation 
Clang - 1ms and ~5mb of RAM for calculation 

2) YEY! My first LeetCode task solved. Believable? It is already

Progress:
- 

---------------


2022-08-9

Today I learned:

Progress:
- reached 1:15:47 of this course - https://www.youtube.com/watch?v=BRuvq59miIo&t=538s

---------------


2022-07-13

Today I learned:

1) I still can think that the tasks can not be that easy.
2) Im still posponing questions to colleagues and after it Im experiencing snowball effect with the tasks. Don't do it, Pablo-Pavlo-Paul. Ask your colleagues!


---------------


2022-06-20

Today I learned:

1) termbin.com - Pastebin for terminal


---------------


2022-05-25

Today I learned:

1) HTTPie - cli postman - https://httpie.io/cli


---------------


2022-04-24

Today I learned:

1) Vim Markdown preview - https://github.com/iamcco/markdown-preview.nvim


---------------


2022-04-23

Today I learned:

1) Exq - queues and schedulers - https://elixircasts.io/elixir-job-processing-with-exq


---------------


2022-04-04

Today I learned:

1) I've lost a streak. It was with me since December 15th 2021 till war starting. 


---------------


2022-03-15
no lectures

Today I learned:

1) https://github.com/ueberauth/ueberauth - Auth with socialnets for Elixir. Plug-based


---------------


2022-03-3
no lectures

Today I learned:

1) Azure instances creating - az vm create -n Virma-az11 -g group-a --image Win2019Datacenter --admin-password %9383% --admin-username %jd% --location centralindia
https://github.com/Azure/azure-cli


---------------


2022-02-17
no lectures

Today I learned:

1) gitconfig aliases. Finally! Now I can use git s, git chn, git ll


---------------


2022-02-05
no lectures

Today I learned:

1) GenServer in a sandbox

---------------


2022-02-04
no lectures

Today I learned:

1) It turns out with "iex --name bla@bla --cookie same_cookie_as_remote_node --remsh this_remote_node@and_ip_address" I can be connected to a node. Mindblowing
2) erlangpl really works. with just ./erlangpl -n name_of_the_node -c same_cookie_as_remote_node

---------------


2022-01-11
no lectures

Today I learned:
1) An issue with root's lost password - 
Solution:
 Reboot your computer
 Hold Shift during boot to start GRUB menu
 Highlight your image and press E to edit
 Find the line starting with "linux" and append rw init=/bin/bash at the end of that line
 Press Ctrl+X to boot.
 Type in passwd username
 Set your password.
 Type in reboot. If that doesn't work, hit Ctrl+Alt+Del

2)  to add yourself in sudoers you need root password and add yourself in visudo


---------------


2022-01-09
no lectures

Today I learned:
1) SAA Exam preparations - https://explore.skillbuilder.aws/learn/course/125/exam-readiness-aws-certified-solutions-architect-associate-digital
2) AWS freelance platform - https://iq.aws.amazon.com/?utm=docs&service=Serverless%20Applications%20Lens

---------------


2022-01-08
no lectures

Today I learned:
1) ready-to-use use-cases for CDK - https://github.com/awslabs/aws-solutions-constructs/tree/main/source/use_cases
updated: more Py-use-cases - https://github.com/aws-samples/aws-cdk-examples/tree/master/python

2) this might be next step for TBC payment processing - https://github.com/aws-samples/aws-cdk-examples/tree/master/python/lambda-layer/



---------------


2022-01-06
15th lecture
Lecture AWS S3

Today I learned:
1) Add MFA to learning and personal accounts
2) Docker works with WordPress and MySQL



---------------


2022-01-05
14th lecture
Lecture AWS services first look + AWS IAM

Today I learned:
1) Edge locations
2) IAM.  MFA means Multi- and not Two-three-Nth factor auth
3) Nice thoughts from http://www.paulgraham.com/raq.html
- Two startups want to hire me. Which should I choose?
Pretend you're an investor—which you are, of your time—and ask yourself which of the two you'd buy stock in.



---------------


2022-01-04
no lectures

Today I learned:
1) Docker-compose for Wordpress... is just working from a box :D That's satisying as hell :)


---------------


2022-01-01
no lectures

Today I learned:
1) 


---------------


2021-12-30
no lectures

Today I learned:
1) AWS CDK >>> cdk synth && cdk deploy && cdk destroy
2) AWS CDK will ask you when it seems to raise your costs for AWS. You are the person who choose
Example I've worked with - https://docs.aws.amazon.com/cdk/v2/guide/ecs_example.html


---------------


2021-12-28
no lectures

Today I learned:
1) AWS documentations and AWS learning videos have not always correct :) I've got problem with TypeScript in learning video which shows old version of code.


---------------


2021-12-27
no lectures

Today I learned:
1) There is the Path inside the AWS. Full-size big-ass Path to your goal with AWS. It's free!


---------------


2021-12-26
no lectures

Today I learned:
1) Alibaba Cloud - AWS from asian world - https://www.alibabacloud.com/pricing?spm=a3c0i.7911826.6791778070.dnavpricing0.794b3870r38JNg
Free trial included
2) Alibaba Cloud learning path - https://www.alibabacloud.com/help/en/doc-detail/86739.html
3) WHole AWS Docs - https://docs.aws.amazon.com
4) Explained and calculated AWS implementations. Ready-to-start with or ready-to-help-sell-AWS-to-the-client implementations - https://aws.amazon.com/solutions/implementations/?solutions-all.sort-by=item.additionalFields.sortDate&solutions-all.sort-order=desc&awsf.Content-Type=*all&awsf.AWS-Product%20Category=*all&awsf.AWS-Industry=*all

---------------


2021-12-25
no lectures

Today I learned:
1) PDF reader with VIM bindings - Zathura
2) AWS learning plans - https://explore.skillbuilder.aws/learn
3) Well-acritectured design principles - https://docs.aws.amazon.com/wellarchitected/latest/analytics-lens/well-architected-design-principles.html

Ideas:


---------------


2021-12-24
AWS class

Today I learned:
1) I've reached first AWS certification

---------------


2021-12-23
no lectures

Today I learned:
1) how to make terminal screencasts - https://asciinema.org/
2) AWS calculator - https://calculator.aws
3) AWS lambda with blank-python - https://github.com/awsdocs/aws-lambda-developer-guide/tree/master/sample-apps/blank-python

---------------


2021-12-20
12th lecture in a row
gitlab-ci

Today I learned:
1) if add a dot to job name - it is the same as comment it. Runner will skip this job

---------------


2021-12-18
12th lecture in a row
2nd lecture soft skills

Today I learned:
1) https://12factor.net/

---------------


2021-12-17
11th lecture in a row
1st lecture CI/CD

Today I learned:
1) https://12factor.net/

---------------


2021-12-13
9th lecture in a row
3st lecture about Gitlab

Today I learned:
1) show Nginx docker-container for localhost 8080 (can be used for local projects) - sudo docker run -t -d -p 8080:80 --name nginx-baby nginx

---------------


2021-12-10
9th lecture in a row
3st lecture about Gitlab

Today I learned:
1) GPG keys. Added it to RIA and PariMatch projects


---------------


2021-12-09
Day-off


Today I learned:
5) For the first time in my life I've got Kubernetes dashboard. Got it by my own (to be honest by https://www.katacoda.com, but whatever... :D )
That's why I had no willing to fall asleep :) Worth it!


---------------


2021-12-08
8th lecture in a row
2st lecture about Gitlab

Today I learned:
1) Google boolean search - https://support.google.com/websearch/answer/2466433?hl=en
2) OhMyZsh for zsh
3) How to write readme correctly - https://editorconfig.org/
4) Easy codeshare with coded in Base64 data - https://github.com/topaz/paste \ https://topaz.github.io/paste/
5) Katacoda (kinda best learning-by-doing classes) - https://www.katacoda.com


---------------


2021-12-06
7th lecture in a row
1st lecture about Gitlab

Today I learned:
1) Bash functions. Donno how to add arguments. UPD: already know :D
2) know how put "pipes" as if-statement


---------------


2021-12-05
Day-off
None

Today I learned:
1) Zines - better way to understand hard concepts
    https://wizardzines.com/zines/bite-size-bash/
2) Vagrant init / Vagrant up / Vagrant ssh
