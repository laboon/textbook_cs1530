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


#### Development


#### Integration and Test


#### Release


#### Maintenance




There are other stages which may be necessary as well, depending on the domain of the software being produced and the methodology used to produce it (specific methodologies will be detailed in the next chapter).

#### External Acceptance

#### Regulatory Checks

#### Deployment

#### External Integration

#### EOL Preparation

#### Customer Support

### The Non-Linearity of Software Development

### Estimation

### Top-Down vs Bottom-Up Design
