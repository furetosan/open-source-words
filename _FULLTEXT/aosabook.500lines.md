500 Lines or Less "What I cannot create, I do not understand." -- Richard Feynman This is the source for the book 500 Lines or Less, the fourth in the Architecture of Open Source Applications series. As with other books in the series, all written material will be covered by the Creative Commons - Attribution license, and all code by the MIT License: please see the license description for details. In addition, all royalties from paid-for versions will all go to Amnesty International. The production of this book has been made possible by the financial support of PagerDuty. Mission Every architect studies family homes, apartments, schools, and other common types of buildings during her training. Equally, every programmer ought to know how a compiler turns text into instructions, how a spreadsheet updates cells, and how a database efficiently persists data. Previous books in the AOSA series have done this by describing the high-level architecture of several mature open-source projects. While the lessons learned from those stories are valuable, they are sometimes difficult to absorb for programmers who have not yet had to build anything at that scale. "500 Lines or Less" focuses on the design decisions and tradeoffs that experienced programmers make when they are writing code: Why divide the application into these particular modules with these particular interfaces? Why use inheritance here and composition there? How do we predict where our program might need to be extended, and how can we make that easy for other programmers? Each chapter consists of a walkthrough of a program that solves a canonical problem in software engineering in at most 500 source lines of code. We hope that the material in this book will help readers understand the varied approaches that engineers take when solving problems in different domains, and will serve as a basis for projects that extend or modify the contributions here. Contributors Name Affiliation Project Online GitHub Mike DiBernardo Wave editorial @mdibernardo mikedebo.ca MichaelDiBernardo Amy Brown indie editorial amyrbrown.ca @amyrbrown amyrbrown Allison Kaptur Dropbox byterun @akaptur akaptur Audrey Tang g0v.tw, Socialtext, Apple spreadsheet @audreyt audreyt Brandon Rhodes Dropbox contingent @brandon_rhodes brandon-rhodes Carl Friedrich Bolz Kings College London object model cfbolz.de @cfbolz cfbolz Cate Huston Image Filter app www.accidentallyincode.com/ @catehstn catehstn Christian Muise University of Melbourne flow-shop @cjmuise haz Daniel Jackson same-origin-policy Daniel Rocco BrightLink Technology contingent @drocco007 drocco007 Dann Toliver Bento Box dagoba danntoliver.com @dann dxnn Dessy Daskalov Nudge Rewards Pedometer www.dessydaskalov.com @dess_e dessy Dethe Elza blockcode dethe Dustin Mitchell Mozilla cluster djmitche Erick Dransch Modeller @ErickDransch EkkiD Eunsuk Kang same-origin-policy Greg Wilson web-server @gvwilson gvwilson Guido van Rossum Dropbox crawler @gvanrossum gvanrossum A. Jesse Jiryu Davis MongoDB crawler @jessejiryudavis ajdavis Jessica Hamrick University of California, Berkeley sampler www.jesshamrick.com @jhamrick jhamrick Leah Hanson Google static analysis @astrieanna astrieanna Leo Zovic event-web-framework Malini Das Twitch ci malinidas.com @malinidas malini Marina Samuel Mozilla ocr www.marinasamuel.com @emtwos emtwo Ned Batchelder edX templating engine nedbatchelder.com @nedbat nedbat Santiago Perez De Rosso same-origin-policy Taavi Burns Previously at Points, now at PagerDuty data-store @jaaaarel taavi Yoav Rubin Microsoft In-memory functional database @yoavrubin yoavrubin Technical Reviewers Amber Yust Andrew Gwozdziewycz Andrew Kuchling Andrew Svetlov Andy Shen Anton Beloglazov Ben Trofatter Borys Pierov Carise Fernandez Charles Stanhope Chris Atlee Chris Seaton Cyryl Płotnicki-Chudyk Dan Langer Dan Shapiro David Pokorny Eric Bouwers Frederic De Groef Graham Lee Gregory Eric Sanderson James OBeirne Jan de Baat Jana Beck Jessica McKellar Jo Van Eyck Joel Crocker Johan Thelin Johannes Fürmann John Morrissey Joseph Kaptur Josh Crompton Joshua T. Corbin Kevin Huang Maggie Zhou Marc Towler Marcin Milewski Marco Lancini Mark Reid Matthias Bussonnier Max Mautner Meggin Kearney Mike Aquino Natalie Black Nick Presta Nikhil Almeida Nolan Prescott Paul Martin Piotr Banaszkiewicz Preston Holmes Pulkit Sethi Rail Aliiev Ronen Narkis Rose Ames Sina Jahan Stefan Turalski William Lachance