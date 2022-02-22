Interview questions
===================

- Who you are and what you do?
- What do you do to secure your emails?
- Check the participant's familiarity with Thunderbird and Enigmail
- How do you exchange keys with your contacts?
- What do you particularly like or dislike in the OpenPGP feature of Thunderbird right now?

Tasks
=====

1. « Send an email using Thunderbird to book a class with your yoga teacher <yoga@irq7.fr>.

Your email: test@irq7.fr
Password: xxxxxx »

Incoming server:

- Protocol: IMAP
- Hostname: mail.potager.org
- Port: 993
- Connection security: SSL
- Authentication method: Autodetect
- Username: test@irq7.fr

Outgoing server:

- Hostname: mail.potager.org
- Port: 465
- Connection security: SSL
- Authentication method: Autodetect
- Username: test@irq7.fr

   - User goals:
     * Warm up
     * Setting up an account
     * Sending an unencrypted email
     * (MAYBE) Setting up OpenPGP encryption
       - We wouldn't prompt the user to do it right now but they might

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
       - « Make sure that I can also send you secure emails. »
       - « Share your key with me so I can answer you with an encrypted email. »
     * To insist on publishing on key servers:
       - « What would you do if you wanted anybody on the Internet to be able to send you encrypted emails? »
       - « Can you think of any other way to make your key available to anybody on the Internet? »
     * Have my phone number ready if they want to check my fingerprint, and then fake a call.

3. « Send me a first encrypted message as a test. » (if not done already)

   - User goals:
     * Accepting a key collected in an email
     * Sending an encrypted and signed email to a single recipient with unaccepted key

4. « I sent you an answer. Check it out! »

   My email includes my public key:

       Subject: secret action on Sunday 23:00 at the Chinese embassy

       I really want you to participate in our secret action this week-end. Can we count on you?

   - User goals:
     * Collecting keys from emails automatically
     * Reading an encrypted and signed email
     * Comprehension of subject encryption

5. « Answer me that you want to join the group. »

6. « On the next day, you have another answer from me in your inbox. Check it out! »

   My email is encrypted but not signed, doesn't quote any previous email and includes:

       Subject: keys for the group

       Hey,

       I'm sending you in attachment, the keys of the people who will
       participate in the action:

       - lucia@irq7.fr
       - gabriel@irq7.fr
       - samira@irq7.fr
       - derwin@irq7.fr

       They are impatient to meet you, please send them an email to introduce
       yourself.

   - The key for Lucia is expired but can be updated online
   - The key for Gabriel is double: his old key and his new key
   - The key for Samira is fake.
   - The key for Derwin is missing.

       gpg --armor --export 0x8B23BF700BA15B54 0x963CB75B6DB79956 0x8D5D4FBF2A8121BB 0x4F12680CEA5CBED5

   - User goals:
     * Accepting a key that was not accepted yet
     * Receiving an encrypted and unsigned email
       - Check whether people realize that it's insecure?
     * Importing keys from a file
     * Collecting keys from emails automatically
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

- Gabriel answers that they can't read as long as keys are accepted.
- Samira answers that she can't read until her correct key is imported.
- Send Gabriel's and Lucia's keys to Samira.

Follow up questions
===================

- Encryption toggle if they went back to the OpenPGP menu regularly
- Key notification if they ignored it at first
- Subject encryption
- Retrospect on the different emails and their security:
  * One of the emails from me was unsafe. Can you find it and why?
  * Encrypted and unsigned email from me.
  * Unreadable email sent to Gabriel and Samira.
- How would you feel about using this everyday for many encrypted emails?
  * How could Thunderbird help you better on a daily basis?
  * Encrypt when possible
  * Never encrypt
- Mockups:
  * Verification
- Account settings

Debriefing questions for the team
=================================

- What did you find interesting, or not so interesting, in the session?
- How would you compare the feedback that we're getting from these tests
  with your usual sources of feedback (BMO, mailing lists, etc.)?

Non-goals
=========

- Detecting a malicious UID in an accepted key
- Sending a signed only email
- Several keys found online (WKD + key server)
- Multiple identities
- S/MIME
