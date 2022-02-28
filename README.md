# zku22 Background Assignment - Notes

	What is a smart contract? How are they deployed? Describe how a smart contract is deployed and the necessary steps
		
		Let's first perhaps describe what a contract is. A contract is an agreement between two or more people, where they agree to do certain things.
		For example, if I work for you, we might sign an employment contract that says, if I do these things, you'll pay me this much money.
		A smart contract is a version of contract that is written but instead of being two people, it could be between two computer programs.
		Smart contracts are deployed using either software interfaces or upon the execution of certain events. 
		In the context of blockchains, smart contracts are typically deployed using cryptographic signatures as a method of 'legally' binding them to each party
		Specific steps to deploy smart contracts could vary - could be via UI, could be upon passage of IRL events, etc.
		Would also be worth mentioning that the code in this case becomes the 'legalese' behind the contract
		SWE SC deployment steps (assuming js and solidity on Ethereum blockchain)
			Utility toolkits/development frameworks that help structure and link various modules together
			Setting up RPC Server
			Writing the contract itself
			Deploying the smart contract to the blockchain instance
			Interact with it using a console or GUI 
			Test the smart contract  using a test framework
			Note: deploying to the mainnet will cost gas fees
	
	What is gas? Why is gas optimization such a big focus when building smart contracts?
	
		Nearly all protocols require gas fees, aka transaction fees, in order to compensate for the cost of validating of the network.
		Some transactions are simple state updates, but others, particularly those with smart contracts, require a bit more 'computational effort' for the verification process to occur.
		Due to the nature of blockchains, only a finite number of transactions can be verified and appended at a given time.
		Furthermore, as protocols get more popular, more and more transactions need to be added to the chain.
		Protocols such as Ethereum have created a process where the sender can choose to pay additional gas fees to prioritize their transaction.
		Unfortunately, these fees have gotten too expensive for most users to use on a day-to-day basis.
		Gas optimization is important because fee minimization is essential to a positive UX, and users will gravitate towards platforms that are less expensive to use (provided their desired features are on these cheaper platforms). What is a network without its users?

	What is a hash? Why do people use hashing to hide information?
	
		A hash (or hash function) is a process whereby information is encrypted (using a variety of methods), and the result is difficult to work backwards from without additional information such as a key
		Hashing is used because it might be the case that important information needs to be sent to someone without fear of this information being intercepted by 3rd parties.
		Hashing has been used for at least 100 years in various forms.
		
	How would you prove to a colorblind person that two different colored objects are actually different colored? Avi Widgerson talk
	
		You could use a third party and a blind test. Go on the street, ask random people, conduct a poll. Develop a large, randomized sample size.
		It seems that random sampling is pretty popular concept in this field. You could optimize the test to minimize liars or cheaters.
		https://www.youtube.com/watch?v=5ovdoxnfFVc&t=4s
			Color maps
				Every planar map can be colored with four colors. But not every map can be colored with three colors
				Put color you need in an envelope
			NP completeness
				Every mathematical statement can be converted into a map
				If statement is true, map is 3-colorable. If false, map is not 3-colorable
			Things we see proofs of don't require trust
