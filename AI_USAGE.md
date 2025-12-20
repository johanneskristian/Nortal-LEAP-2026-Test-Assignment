# AI Usage

Briefly describe how you used AI (tools, prompts, code snippets, fixes). Be concise and honest (using AI is fine; it's just a tool; we want to know your method). If you did not use AI, state that here.

I had half of the logic written to prevent direct borrowing when a book is reserved, but I struggled to complete the logic that checks whether the user is first in the reservation queue. 
I used AI to ask how to determine if a user is first in the queue. AI’s answer did not match my implementation, but it helped me understand how to access the reservation list and compare the first entry with the user ID.

I struggled to understand why my code was not working and kept returning invalid responses when checking whether the member returning a book was the actual borrower. 
I used AI to help debug the issue and discovered that the problem was related to the frontend sending an incorrect memberId. 
Since the assignment allowed changes only to the backend, I was very confused for a long time. I joined the Nortal assignment Discord where many others had the same issue,
and I decided to modify the frontend so that the returnBook method sends the correct memberId value.