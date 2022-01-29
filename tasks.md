Tasks
=====

1. « Send an email using Thunderbird to book a class with your yoga teacher yoga@irq7.fr. Your email: test@irq7.fr, Password: mic7Ega2. »

   - User goals:
     * Setting up an account
     * Sending an unencrypted email
     * (MAYBE) Setting up OpenPGP encryption
       - We wouldn't prompt the user to do it right now but they might
   - It's kind of a warm up task

2. « Set up everything you need to exchange very sensitive information with me <nf@irq7.fr> over email. »

   - User goals:
     * Setting up OpenPGP encryption
     * Sending public key
     * (MAYBE) Sending an encrypted and signed email to a single recipient with missing key
     * (MAYBE) Verifying a fingerprint
       - We wouldn't prompt the user to verify the keys but they might do it by themselves.
     * (MAYBE) Discovering key online
   - Stepped tasks (that we could use to direct the user more):
     * To insist on sending public key:
       - « Make sure that yyy@yyy.com can also send you secure emails. »
       - « Share your key with yyy@yyy.com so they can answer to you encrypted emails. »
     * To insist on publishing on key servers:
       - « What would you do if you wanted anybody on the Internet to be able to send you encrypted emails? »
       - « Can you think of any other way to make your key available to anybody on the Internet? »
     * Have my phone number ready if they want to check my fingerprint, and then fake a call.

3. « Send me a first encrypted message as a test. » (IF NEEDED)

   - User goals:
     * Accepting a key collected in an email
     * Sending an encrypted and signed email to a single recipient with unaccepted key

4. « You received an answer from me. Check it out! »

   - My email includes my public key
   - Subject: "secret action on Tuesday, 145 Main Street"
   - « I really want you to participate in our secret action next week. Can we count on you? »
   - User goals:
     * Collecting keys from emails automatically (if in prototype)
     * Accepting a key that was not accepted yet
     * Reading an encrypted and signed email
     * Comprehension of subject encryption

5. « Answer me that you want to join the group. »

6. « On the next day, you have another an answer from me in your inbox. Check it out! »

   - My email is encrypted but not signed, doesn't quote the other email, and includes:
     * eileen@irq7.fr	0x1334ECDD57B0C88D	expired key that can be updated online
     * gabriel@irq7.fr	0xBC5C4FF9DE1561F8	old key
                        0xAC9DF9562BF7DA2C	new key
     * samira@irq7.fr	0x8ACA30119C2AE124	fake key
     * derwin@irq7.fr	0x62526A337AD1AA17	missing and not online
     * Phone numbers for everybody
   - User goals:
     * Receiving an encrypted and unsigned email
       - Check whether people realize that it's insecure?
     * Importing keys from a file
     * Collecting keys from emails automatically (if in prototype)
     * Comprehension of encrypted but not signed

6. « Send an encrypted email to the group to introduce yourself. »

   - Goals:
     * Send an encrypted and signed email to multiple recipients with issues
     * Solving a missing key
       - (MAYBE) Online key discovery
         * 1 failure to see what people would do in this case
     * Updating an expired key
       - (MAYBE) Online key discovery
         * 1 success
         * 1 failure
     * Solving conflicting keys: choose between the older and newer key for the same address
   - Key found online and other key collected from email

Optional tasks
==============

- Online key discovery
- Gabriel can't read as long as both keys are accepted
- Samira can't read until correct key is imported

Non-goals
=========

- Detecting a malicious UID in an accepted key
- Sending a signed only email
- Several keys found online (WKD + key server)
- Multiple identities
- S/MIME

Interview questions
===================

- What do you do to secure your emails?
- How do you exchange keys with your contacts?
- What is most annoying to you in the OpenPGP feature of Thunderbird right now?
