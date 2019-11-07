# Identity Hub Service

Pfalfa Identity served as decentralized identity hub inside Pfalfa Platform. It's based on decentralized, peer to peer with public/private key cryptography [GunDB SEA API](https://gun.eco/docs/SEA)

It feature similar to what centralized services offer such as Facebook Login but with fundamentally difference on the backend since Pfalfa will not store password/private key in the server nor transport between server. The private key of user will be kept on the user device.

Pfalfa Identity Hub Service can be used all across the platform for developer to integrate using API, as well as end-user who'd like to use any of dApps under Pfalfa Platform.

## Technology

### What is Decentralized Identity

> Identity is one of the most vital pieces when it comes to the management of user-specific information. With identity theft turning into a major concern nowadays, there is a need to ensure that identity of a human or a machine is self-sovereign and hack-proof. Owning to a huge amount of data associated with identities, there is also a need to ensure that the systems handling identity-related data are capable of handling high scale. That is where Pfalfa comes in as a natural fit for solving identity-related issues because of its combined characteristics of blockchain and database.

A key piece to decentralized identity is how people, devices, and other entities in the world are identified without a centrally owned registry. Decentralized identity re-envisions the way people share access, control, and share their personal information. It gives people power back over their identity.

### How it Work

To create a new user account, it first generate a public/private key pair. then it add the ability to login to the account by hashing the password and a salt with PBKDF2. This produces a proof of work that is used to encrypt and decrypt the private key with AES.

Once we have the private key, it can then read and write our own personal data using the private key as an AES encryption key. We can also have private conversations with others by sending them our public key padlock.

Finally, we can prove to others we said something by adding a digital signature to our published content, which the public key can then verify.

### Data Security

Most websites you use today have fake security. When you log onto their service, your password gets sent up to their proprietary servers. There they check to see if it is correct and grant you access to YOUR data.

Sure, their servers might be in a top secret location. But the problem is that they know your password. Which means any bad actor, like a rogue employee, a hacker, or a government agency can snoop on your data without you knowing.

So what does real security look like?

Rather than your password getting broadcast over the internet, you instead get sent a bullet proof vault that you try to open. If your password is correct, the vault unlocks. But if you are a hacker, it would take a 100 years to crack open - and you would have to do this for EVERY piece of data sent to you.

This makes it very hard for bad actors to spy on you because your password never leaves your computer.

### Cryptography

The most important piece is first creating user accounts. Unfortunately, a username/password combo is not very secure. We need something better.

During the Cold War a new type of security was invented. It is similar to a username/password, but imagine instead having to memorize the first thousand digits of PI! Having a password that long would take a hacker one hundred years to break. This is why it is secure and it is called public/private key cryptography.

However, your users would probably get really confused with that. So how can we let them keep their own password... but still have real security? Well, we take their normal password and mix with other information. The end result is long and complicated, creating a secure account for our users to sign into.

### Proof of Work

It might be easy for you to guess what the other ingredients are. But you would still have to bake a pie for each guess. That is a lot of extra work. And that is exactly why mixing our password with some salt* keeps our account secure. This recipe is called Password Based Key Derivation Function number Two or PBKDF2 for short.

If you know the password, it is easy to bake the same pie again and again. If you don't know the password, guessing is easy, but baking is hard. This idea is called "proof of work" and is important for creating and signing into a user account.

### Encryption

So far, we created a user account with public/private key cryptography. This way, it is secure, unlike passwords. We then used PBKDF2 to extend the user's password into a "proof of work". That way, if a hacker tries to guess the password, they have to do hours of extra work for every guess.

Now, we use the proof of work to decrypt the private key. This private key is used to lock and unlock our private data, in the same way you lock your house or car to stop other people from getting at your stuff. But, how does a lock work?

Encryption is the same thing, it rotates each letter by a different distance, thus scrambling the message. You can only unscramble the message if you have a key that perfectly restores every letter in the message. This is called Advanced Encryption Standard, or AES for short.

### Public Private Key

It is easy to confuse encryption keys and public/private keys. One is like a door knob, you need a key to both lock and unlock it. While public/private keys are like a padlock, the public key can close the lock but only the private key can open it.

This becomes useful when we want to have a private conversation. Alice and Bob exchange padlocks. Now Alice can write a message that only Bob can open. When Bob replies to Alice, he uses her padlock so only she can open his message.

Simple enough, but what if we want to have a group conversation? Alice creates 4 copies of an encryption key, which will let everybody in the group both lock and unlock. She now can invite Bob, Carl, and Dave to the group by sending them the key by using their individual padlocks.

Once everybody has the same shared key, they can now write and lock a message to the group that only the group can see. Allowing everybody to pass messages around. 
