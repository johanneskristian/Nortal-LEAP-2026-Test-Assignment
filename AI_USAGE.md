# AI Usage

Briefly describe how you used AI (tools, prompts, code snippets, fixes). Be concise and honest (using AI is fine; it's just a tool; we want to know your method). If you did not use AI, state that here.

# Prevent double loans and respect queues
(A book already on loan must not be loaned again.) - Did not use AI
(No line-jumping via direct borrow.) - I had half of the logic written to prevent direct borrowing when a book is reserved, but I struggled to complete the logic that checks whether the user is first in the reservation queue. I used ChatGPT to ask how to determine if a user is first in the queue. AI’s answer did not match my implementation, but it helped me understand how to access the reservation list and compare the first entry with the user ID.
(Returns should only succeed when initiated by the current borrower.) - Did not use AI

# Reservation lifecycle
(Duplicate reservations by the same member should be rejected.) - Did not use AI
(Reserving an available book should immediately loan it to the reserver if eligible) - Did not use AI
(Returning a book must hand it to the next eligible reserver in order) - I struggled to understand why my code was not working and kept returning invalid responses when checking whether the member returning a book was the actual borrower. 
I used Gemini AI to help debug the issue and discovered that the problem was related to the frontend sending an incorrect memberId. 
Since the assignment allowed changes only to the backend, I was very confused for a long time. I decided to modify the frontend so that the returnBook method sends the correct memberId value.
(Skip ineligible/missing members and continue) - I had implemented automatic borrowing to eligible reservers but did not know how to skip ineligible members and continue. So I asked Gemini AI how to do it and figured out what I needed to add in front of my implemented feature to skip ineligible members.
(Keep the queue consistent when handoffs happen.) - Did not use AI

# Borrow-limit enforcement & clarity
This was really hard for me. After a long time googling how to do it and my code not working, I decided to use Gemini AI to find out how to approach implementing borrow limit enforcement. It helped me replace the inefficient findAll() with a more efficient countByLoanedTo method in the repository.