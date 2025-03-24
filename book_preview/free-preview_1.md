# Awareness for Employees & Business Owners

Regardless of who you are and what you do, these are all practices that are **extremely important** to understand in improving how you interact with the online world.

## Understanding IP Addresses

Before we begin, the most important first concept is an **IP address**. Think of an IP address as your home's street address, but for the internet. Your **public IP address** is what allows your devices to connect to websites and online services. Without it, you would be invisible online and unable to send or receive any information like your mail box recieving packages or sending mail.

This address is issued by your ISP (Internet Service Provider) and is **unique per household** not per device. A public IP will usually look like this: 

`172.217.24.46`

## Key Networking Concepts

There are 2 other main distinctions we can briefly touch on for now until going into depth later:

### DNS (Domain Name System)

When you type in and connect to a website like `google.com`, this is known as a **DNS** (Domain Name System). It's unrealistic for people to remember `172.217.24.46` the public IP address when they access the internet, so a DNS resolver is used to convert `google.com` to `172.217.24.46`. 

> Think of it like your contacts list in a cellphone, you can't be expected to remember EVERY phone number but by giving them names you recognize, you can now know who to call or text.

### How Websites Connect

With that in mind, whenever you access a website:
- Your **Public IP** is connecting to their **Public IP**
- At this early stage of your learning it's best to just simply say - yes you can run a website directly from your phone or computer inside your network 
- People can see it and connect to it by entering your public IP instead of a DNS (You'll learn more about this later)
- Then you can imagine buying a domain like `my-personal-website-and-stuff.com` and through a DNS provider point it to your public IP

### Private IP Addresses

The last and final note before we begin is **private IP addresses** or **internal IP addresses**. These are used internally on your network between your phones, computers and other devices to know which devices to send the internet traffic to and from. 

Essentially ensuring that when one user searches Google, another device on the network can also be doing something entirely different.

---

**Learning the distinction between internal/private IPs and public IPs is fundamental to understanding networking concepts, identifying malware threats, and recognizing common attack vectors. This foundational knowledge serves as an essential building block for the more advanced concepts we'll explore later. Consider this your gateway to deeper networking expertise.**

# Scam Messages and Phishing Attacks

## Introduction
One of the most common attacks against businesses and employees is **Phishing**. Along with phishing, however, it's important to discuss **Whaling**, **Smishing**, and **Vishing**. All of these are used by hackers as well as scammers to exploit basic human nature, mainly **curiosity** and **urgency**.

## What is Phishing?

Phishing is a type of cyber attack where criminals trick you into giving away sensitive personal information like passwords, credit card details, or account access. The attackers do this by pretending to be trustworthy organizations or people you know.

Typically, phishing operates in one of two ways:
- Creating a fake website that looks identical to a legitimate one (like your bank or social media), or
- Building a new website that targets your specific interests such as hobbies, entertainment, or professional needs.

Through these fake sites, attackers can capture your personal information when you attempt to log in or make purchases.

They can also be seen purchasing advertisements on google and social media to promote their fake websites to people that match your interests and age range. Advertising campaigns can get extremely specific all the way from gender to age, down to city or even street sometimes.

## How Phishing Sites Work
The way these sites usually work is:

1. **Initial Access**: Get you onto their website using whatever method best fits you as shown previously.
2. **Data Collection**: You enter your details, click Next to submit it to either sign-in or register (sign-up)
3. **Backend Storage**: That data is saved to a backend web panel/admin for the hackers to see in plaintext (ordinary readable text)
4. **Attacker Alert**: The webpage will take a while to load usually showing a throbber (spinning icon/loading icon) while the attacker gets a ping (loud noise) in the backend which alerts them to pay attention
5. **Credential Use**: They can now decide what to do with these details:
   - Usually they forward your credentials manually to login to the real portal/website
   - Or simply try to use your card details somewhere else to buy something if you put in your credit card details
6. **Misdirection**: All in the meantime, your browser will 'pretend' to be loading until the hackers click a button to proceed you to the next page, which oftentimes will redirect you to the official/real website they are impersonating.

### 2FA Interception Process
When attackers capture your login information, they can also intercept your two-factor authentication (2FA) codes. Here's how this works:

1. The attackers use a "backend panel" - which is essentially their control screen where they monitor and manage their attacks (Think of it like a user account on facebook but for an administrator to see other data).

2. When they attempt to login to the real website using your stolen credentials, this triggers the legitimate 2FA system to send you a text message or email with a verification code.

3. Meanwhile, on the fake website you're still using, you'll see a new prompt asking for this code.

4. When you receive the legitimate verification code from the real service (like Facebook), you naturally assume your login is proceeding normally.

5. You enter the code on the fake site, which the attackers then capture and use to complete their login to your real account.

After this process is completed, the attackers usually redirect you to the real website. You might see an error message saying you mistyped your password, making you think you simply need to login again. When you try again on the real site, it works normally - leaving you with no idea your account has been compromised.

# Understanding Phishing Attacks

## A More Typical Phishing Attack Flow Example

1. You receive an email from one of the following or potentially for some mistype the URL called **Typosquatting**, the act of 'squatting' on a domain and holding it until someone reaches it rather than actively sending it to people (Keep in mind all are fake and impersonating Facebook)

    | Type | Example | Description |
    |------|---------|-------------|
    | **Homoglyph** | facebooⱪ.com | The letter K is replaced with ⱪ |
    | **Subdomain Impersonation** | verification-facebook.com | A real example would be `verification.facebook.com` |
    | **Another Subdomain** | faceb.ook.com | The real website  in this instance is `ook.com` with a subdomain of `faceb` |
    | **TLD Swap** | facebook.pw | Where the 'top level domain' com is pw in this instance |
    | **Vowel Swap** | faceboak.com | Changing a vowel |
    | **Omission** | faceook.com | Removing a letter |
    | **Insertion** | facebiook.com | Adding an extra letter |
    | **Character Replacement** | facelook.com | Replacing one character with another |
    | **URL Extension** | facebook.com.webportal.securesitelogin.com | Multiple subdomains to extend past visible URL length |
    | **Character Reversal** | facedook.com | Character reversal for b becoming d |

2. You enter your details thinking it is legitimate
3. This alerts the attacker in the backend panel with other information such as your IP address, computer specifications (GPU, CPU, Timezone, Internet browser being used and a list of other minor fingerprinting items) (Fingerprinting being the term used to decribe collecting information to identify a specific person or device out of others)
4. The attacker copies the details that you just entered such as credentials and attempts to login to the real website using an IP within your country or city.
5. If the attacker is prompted by your bank for example with a request for a text message or email code, they will press that button in their backend panel
6. You will now get a popup to enter your code you received
7. The attacker copies the code from the backend that you just entered to finish their own login session
8. If the information was incorrect at any stage, the attacker will 'resend' a request to you to say it was invalid
9. After all is said and done, you will be forwarded to the final destination of the real website - usually logged out unless they can craft a direct login URL for you to access
10. During this period you will be simply waiting for the website to load

Not all phishing websites handle the real-time communication like this; some simply take your information as you enter it, then store and forward you to the real website.

Now let's look at another way they can make it more convincing. Imagine you receive an email saying your account has been suspended with a link - looking like a completely legitimate email to the untrained eye - no spelling errors, correct footers, logos and maybe even emails and phone numbers. But the link in the email to recover your account from the support portal might be something like `support.recovery-facebook.com/John.Smith` - in this instance, John Smith being your real name/username on the service. This would require the attacker to have made the connection from your email to your username but I digress. 

When you click the button to recover your account, it autopopulates the fields with known information about you such as age, username, email, profile picture and even friends. This can make it extremely convincing that this is the real service.

## Common Phishing Tactics
Other vectors to look out for.

### 1. Creating False Urgency
Attackers deliberately use urgent language to pressure you into acting quickly before you can think critically.

Common urgent phrases in phishing emails include:
- "Please take immediate action"
- "24 hours to respond"
- "Final opportunity"
- "Quick response needed"
- "Emergency"

When you feel rushed, you're more likely to make mistakes and overlook warning signs that something isn't right.

---

### 2. Fake Mobile Apps
Attackers create counterfeit versions of popular apps that look almost identical to the real thing.

These fake apps can appear in official app stores like Google Play or Apple's App Store, despite their security measures. They can also be distributed through:
- Social media links
- Third-party app stores
- Direct download links in emails or messages

On Android devices, installing apps from unknown sources requires changing your security settings. While this is blocked by default (for your protection), many people disable this security feature without understanding the risks involved.

These fake apps often request excessive permissions and can steal your personal information, display unwanted ads, or even lock your device and demand payment (ransomware).

---

### 3. QR Code Phishing
Those black and white square patterns you scan with your phone can be used by attackers to trick you.

What are QR codes? Think of them like barcodes in stores, but instead of just identifying a product, they can contain actual information like website addresses or commands for your phone. When you scan them with your phone's camera, they can instantly open websites or perform actions.

Attackers exploit this convenience by placing fake QR codes in public places like:
- On parking meters or transit stops (claiming to be for payment)
- In coffee shops (pretending to be for Wi-Fi access or rewards)
- On posters or flyers (offering promotions or information)
- In emails (disguised as package delivery information)
- On clothing so if anyone tries to take your picture, some camera apps will automatically try to scan the code.

When you scan these codes, they take you to fake websites designed to steal your login information or payment details.

A real-world example happened with Discord (a popular chat application). Discord lets users sign in on their computer by scanning a QR code with their phone. Attackers would create fake promotions telling users to scan special QR codes for rewards. When users scanned these codes, they weren't getting rewards—they were unknowingly giving attackers access to their accounts.

---

### 4. Search Engine Phishing
This involves attackers using online ads to place their malicious sites at the top of your search results.

When you search for something online, you often see "sponsored" or "ad" results at the top. Legitimate businesses pay for these spots to get noticed, but attackers can do the same thing with fake websites.

Here's what makes this especially dangerous: In these ads, what you see isn't always what you get. For example, an ad might display "https://facebook.com" in the visible link, making you think you're going to the real Facebook site. However, when you click it, you're actually sent to the attacker's fake site that looks identical to Facebook.

Attackers also use a technique called "backlinks" to make their fake sites appear more trustworthy. They hack into legitimate websites and hide invisible links to their malicious sites. This tricks search engines into thinking the fake site is popular and trustworthy, pushing it higher in your search results.

---

### 5. Tech Support and Impersonation Calls
These attacks involve someone calling your workplace and pretending to be a colleague or vendor who needs access to information.

How it works:
- The attacker researches your company to learn employee names, departments, and current projects
- They call your workplace with a convincing story, using insider information to build trust
- For example, they might say: "Hi, this is Mark from IT. Sarah in accounting asked me to get the pre-release materials for next week's product launch."

Without proper security protocols, this technique can be surprisingly effective. Through these calls, attackers might:
- Get their passwords reset
- Have new accounts created for them
- Be given temporary access to another employee's credentials
- Obtain confidential documents or information

What makes this attack dangerous is how it exploits human helpfulness and uses specific company details to appear legitimate.

---

### 6. Email Thread Hijacking
This is when attackers trick you by inserting themselves into email conversations you're already having. Imagine you've been emailing with your colleague about an invoice, and suddenly "they" send you a message with updated payment information - except it's actually an attacker pretending to be your colleague.

These attackers use several methods to pull this off:

- They might hack into someone's email account first. Once inside, they quietly monitor conversations, looking especially for discussions about money, vendors, or executive decisions. Then, at just the right moment, they jump in and make a subtle change - like sending "updated" banking details just before a payment is about to happen.

- Another method that can be utilized is to copy a subject line that is leaked in a screenshot, video or any means available and even better if you can see other emails associated - You can create a new email thread that looks like it's a continuation of a previous conversation allowing you to insert yourself inside and gain trust by responding at correct times (using an email that's inconspicuous).

Malware distribution through hijacked threads has become increasingly sophisticated. Rather than sending obvious spam with suspicious attachments, attackers respond within trusted email chains with messages like "Here's the updated version we discussed" accompanied by malicious files. Because you trust the conversation, you're more likely to open these dangerous attachments.

---

### 7. Open Redirects
An Open redirect on facebook.com if found can be used such as the login page for https://facebook.com/login.php?redirect=attackerwebsite.com (Example URL) - this would mean if you try signin on the real facebook, after sign in it would redirect you to the attackers website where they can simply say your entered credentials are incorrect and you will try sign in again after already verifying the domain previously.

---

### 8. Document-based Phishing with Embedded Programs
This is when attackers send you documents (like Word files) that contain hidden automated programs (called "macros").

Here's how it works: You open what looks like a normal document, perhaps something important like a contract or paycheck. Suddenly, you see what appears to be a Gmail sign-in window within the document. The document might claim you need to "sign in to view protected content." If you enter your email and password, you're not actually signing into Gmail - you're sending your login information directly to attackers.

These hidden programs in documents are particularly sneaky because most people don't expect a document to contain a login screen, making this a rare but extremely effective attack method.


## Main Types of Phishing

- **Spear Phishing**: A targeted attack against a specific person. Think of a spear point for one target.
- **Whaling**: Targeting important people, CEOs, Executives, etc. Whale being a large target.
- **Smishing**: SMS phishing (via text message).
- **Vishing**: Done via phone call, simply requesting information and using any knowledge you have about inside software, employees, and infrastructure to craft a convincing story to get information out of staff. We have also seen a rise of people using AI voice cloning to achieve better results by finding social media videos or even going in person to talk with employees to clone their voices. With less than 20 seconds of clear audio from someone such as social media or meeting in person - that voice can be used to train an AI model ready for impersonation.

## Where Does the Data Go?
Modern phishing pages are often seen sending usernames and passwords to Discord, Telegram (Chat/Messaging platforms), and anywhere a request can be sent. This is due to domains and web servers often being taken offline after being reported as well as for live updates on their current victims. It can be quite scary for an outsider seeing this in action; thousands of credentials being sent directly to a live chat ready to be sold or used. 

Malware campaigns also follow a similar pattern as phishing. Either via impersonating legitimate domains and software or directly emailing you impersonating an important figure or authority. 

Imagine replacing a phishing link like we discussed with a file to download instead. This can be seen with fake browser updates requiring you to install a file before a website will load or buying ads like previously mentioned but for fake software.

Before we look at some methods to identify phishing emails, it's also important to understand facebook marketplace phishing attempts that have been appearing as those will be more and more relevant as the days go on. Let's say you are purchasing an item or selling an item. The person you will be in contact with will offer to pay for the shipping automatically and send you to a fake shipping website that is a clone of one you might be familiar with. Upon doing so, it will have any details about the purchase or exchange from facebook as they have put it there manually - making it more convincing. It will ask you to signup to get the tracking number or find out how to ship the item and upon doing so your credentials will be 'harvested' by the attacker.

Credential reuse is a common vector we will look at in the future but just keep in mind for now that any usernames, passwords or emails you enter if obtained by a hacker will be used against thousands of other websites to check for accounts they can utilize to their benefit.
