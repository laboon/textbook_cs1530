## Developing A Software Product


When beginning a new software project, it is im

### Who Is Involved In Software Development?

### The Software Development Life Cycle (SDLC)

All software starts as an idea.  Eventually, it needs to be an actual system that people can use.  Along the way, there are numerous phases that software needs to go through in order to reach that final stage.  These phases, and the process of creating the software in general, is known as the _software development life cycle_, often acronymized as the _SDLC_.

Although the software development life cycle as presented below is a Platonic, idealized version.  As we shall see, developing software is often a messy process!  While you may not follow these steps in this particular order, or may combine different steps, similar events and phases will occur in virtually any non-trivial software product.  

1. Analysis
1. Requirements
1. Design
1. Development
1. Integration and Test
1. Release
1. Maintenance

Now that we've seen an overview of the SDLC, Let's look at each of the phases individually.

#### Analysis

__Analysis__ involves determining the needs of the customer and user of the software, researching the __domain__ (the specific field for which the software is being written), and understanding the limitations of the potential software system.  

Often, the end user of the software may not have a detailed idea of the system to be developed.  They may have a general outline, or know what they want it to not do, but will rarely be able to give you a document which specifies everything including what to do in various __edge cases__ (states of the system which are unusual or unexpected in normal operation).  This can be confusing to new software developers, who must be able to distill the general ideas given by the customer to the specific details that are necessary to program a solution.  In the chapter on Eliciting Requirements, there are several techniques to do exactly this.

One of the most interesting aspects of software development is that it can produce systems which help people in many other domains.  For example, I have written programs that controlled radars, kept track of medical records, and helped elementary school children learn mathematics, amongst many others.  For each of these systems, it was not enough to know about programming.  I also had to understand how other systems worked and how to interact with them.  I had to learn standard terminology in that domain (for example, in the finance domain, _SMB_ means "small- to medium-sized business", whereas in the file sharing world, it means "Server Message Block protocol").  

During the analysis phase, you will have to familiarize yourself with the domain in which you are working.  Although it may seem that as a software developer, you can just worry about the code you write, this can get you into trouble.  Remember that programming is a means to an end; no end user cares about what language you used to write the software system in, only that it does what they want.  If you and your team don't understand that domain, you will have great difficulty developing software that can solve the problems of people working in that domain.  You may make assumptions that are entirely contrary to how your users think, and even be unaware that you are making an assumption.  This will make it more difficult for you to create a successful software system.

Finally, the software development team should understand what can and cannot be done.  For example, due to HIPAA regulations, there are legal requirements on what kind of personally identifiable medical information can be stored, and how.  A customer may ask for something which is legally - or physically - impossible to do.  They may not understand what is easy and what is difficult to do from a programming perspective, and thus prioritize poorly.  

After you or your team have analyzed the problem that is being faced by the customer or user, you can move on to the __requirements__ phase.

#### Requirements

The problem space and potential systems have been analyzed, and so now it is time to formalize what you have decided to do and list them as requirements.  Requirements state specifically what the completed system needs to do and be in order to be considered complete.

This phase should also consist of planning for the __verification__ and __validation__ of the requirements.  Verification is checking that you have built the software right; that is, that it meets all of the requirements, performs accurate computation, displays the correct answer, etc.  Validation is checking that you built the right software; that is, ensuring that what you have built meets the needs of the customer.  Your requirements should always be testable in some way.

Before considering this phase complete, it is important to minimize ambiguity and contradiction in the requirements.  While it may be impossible to entirely remove ambiguity in a natural language such as English, especially on a product that was not formally specified in the first place, ambiguity in requirements can cause many issues later on in the process.  Even worse is encountering requirements which contradict each other, or the laws of the Universe.

Once the system has been defined, you can move on to the __design__ phase.

#### Design

After you have determined _what_ the system needs to do in the requirements phase, it is now time to start mapping out _how_ it will be done.  Depending on the methodology, domain, team, and product, this may involve anything from sketching out major subsystems and interfaces, all the way to describing individual classes and methods to be implemented.  Some design of the system is always a part of software engineering, however, even if it is in a single programmer's head.

At a bare minimum, the external interfaces should be planned, and the .  For a command line application, this may mean deciding what command-line switches should be developed, what kinds of interaction the user will have, and whether or not they should be automatable.  For a graphical user application, it may mean designing the user interface.  For large systems, it may include definitions of various subsystems and how they will interact and communicate.

Most design phases will include at least a rough idea of what architectural paradigms will be used.  This will allow a general idea for all developers of how their individual classes and packages are supposed to be laid out, and the basics of how they should communicate with each other.

Code style guides and other rules for development, such as determining how work will be allocated and how to communicate with other members of the team, will be set out.  While many of these may seem minor - does it really matter whether an individual programmer uses tabs or spaces? - it is usually better to set them down now, to avoid confusion later.  For example, if one programmer's editor consistently converts tab to spaces, and another's always does the opposite, this will mean that any time a different programmer edits a file, it will show changes being made to all lines in the file that have any indentation.  This will make it much more difficult to trace what actual changes were made by each developer.

After the design phase is complete, it is time to move on to the __development__ phase.

#### Development

Congratulations!  You have now reached the first part of the SDLC where you will actually get to write code.  Unlike many simple projects, non-trivial software engineering requires much more work than just writing code.  While programming is, of course, an important aspect of software development, it is certainly not the only one.

Developers and other team members will work on determining which programming languages, frameworks, and other tools will be used to develop the application.  The choices can often be more difficult than they appear.  At large or established companies, there may be "standard" or "approved" programming languages or tools, but for a startup or a more flexible team, there may be no precursors to use as a template.  The domain may dictate the language, or at least constrict the choices - for example, most web applications will use some JavaScript since it runs on virtually every web browser.  Even then, though, there are choices to be made.  Should the backend also be in JavaScript using node.js, or should it be in a different language?  Should "pure" JavaScript, or a language which compiles to JavaScript such as TypeScript or CoffeeScript?  Should a heavy front-end framework be used, or should the code be developed while minimizing external dependencies?  There are benefits and drawbacks to each choice, and there are many choices.  And this is for a domain where your choices are relatively restricted!  A desktop application may easily be written in one of dozens of languages.  The decisions you make will depend upon the team you are working with, their background, your goals and timeline for the current project, what libraries are available in those languages, and a myriad of other reasons.

At this point, developers should have a good idea of what the system is supposed to do (from the requirements phase), and a "guidebook" on how to do it (from the design phase).  Developers and managers can determine what parts of the system should be worked on first, either because they are of high business value or because other parts of the system depend upon them.  For example, when developing a user-facing application, perhaps the __graphical user interface__ (__GUI__) basics will be implemented first, so that additional features which will also be displayed graphically can then be constructed using that foundation.  In another situation, when developing scientific modeling software, the best path forward might be to develop the algorithms first, and then build a user interface which interacts with them afterwards.

During the development of the software, many tactical decisions will have to be made as well.  Developers will need to determine the best algorithms and data structures to use, how to comment their code, which external libraries to use, which version of the language to use, how to structure interfaces, and many other things.  There are usually no entirely correct answers to any of these questions, but most will involve trade-offs of one kind or another.  For example, using the newest version of a language may mean that you can use a particular library, but staying with an older version will mean more stability and less training time for the development team.

Of course, software developers do not operate in a vacuum, nor do they always create software which does exactly what it is supposed to do without error and without fail.  That is why the next phase is necessary.

#### Integration and Test

During integration and test, different subsystems and features are integrated to ensure that they work together properly.  

#### Release

Finally, you have written all of the code for your software product, integrated all of the pieces together, and even tested it to ensure that you have as few defects as possible.  While you may be tempted to sit back and rest on your laurels, there's still more work to do be done!  The software has to be released.  


#### Maintenance

The software has been released and is being used, but that does not mean that our hard-working team gets to take a break.  


There are other stages which may be necessary as well, depending on the domain of the software being produced and the methodology used to produce it (specific methodologies will be detailed in the next chapter).  

#### External Acceptance



#### Regulatory Checks

#### Deployment

#### External Integration

#### EOL Preparation

#### Customer Support

### Trade-Offs

### The Non-Linearity of Software Development

### Estimation

### Top-Down vs Bottom-Up Design
