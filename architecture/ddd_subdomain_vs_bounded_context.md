# VS

Subdomains are part of the problem space (what the business does),
while Bounded Contexts are part of the solution space (how software is designed)


Domain in DDD represent *real problem in business*. Such as: E commerce is a domain, Payroll system is a domain
Domain is divided into many sub domains, so each sub domains focus smaller problems. Such as: E commerce has many sub domains such as: Shopping Cart, Billing, Product Catalog, Customer Information...
Each sub domain should have explicit responsibilities so it has a boundary to limit their functionalities, the boundary will help sub domain focus to do only 1 thing and do well. This boundary is considered as bounded context of the sub domain. The bounded context will define:

    How many domain models needed for the sub domain?
    Which properties needed in the each model?
    Which functionalities needed in sub domain?

