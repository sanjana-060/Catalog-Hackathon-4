# Catalog-Hackathon-5

###Voting case scenario to implement it in a simple and easy manner without fraud.

///The code for implementation of the voting system to prevent fraud and to ensure smooth voting..

-----The functions used in this case scenario include--

1)Voter registration

2)Vote casting

3)Vote counting

class VotingSystem:
    def __init__(self, candidates):
        self.candidates = {candidate: 0 for candidate in candidates}
        self.registered_voters = set()  # To store registered voters
        self.voted_voters = set()       # To store voters who have already voted
    def register_voter(self, voter_id):
        if voter_id in self.registered_voters:
            print(f"Voter {voter_id} is already registered.")
        else:
            self.registered_voters.add(voter_id)
            print(f"Voter {voter_id} registered successfully.")
    def cast_vote(self, voter_id, candidate):
        # Ensure the voter is registered and hasn't voted yet
        if voter_id not in self.registered_voters:
            print("You are not a registered voter.")
        elif voter_id in self.voted_voters:
            print("You have already voted.")
        elif candidate not in self.candidates:
            print(f"Candidate {candidate} is not valid.")
        else:
            # Record the vote
            self.candidates[candidate]+= 1
            self.voted_voters.add(voter_id)
            print(f"Vote for {candidate} cast successfully.")
     def tally_votes(self):
        # Print the vote counts for all candidates
        print("\nVote Tally:")
        for candidate,votes in self.candidates.items():
            print(f"{candidate}: {votes} votes")
     def get_winner(self):
        #candidate with the most votes
        winner = max(self.candidates,key=self.candidates.get)
        print(f"\nWinner: {winner}")

candidates=["Ana","anjali","Sanjana"]
voting_system =VotingSystem(candidates)

voting_system.register_voter("Voter1")
voting_system.register_voter("Voter2")
voting_system.cast_vote("Voter1","Ana")
voting_system.cast_vote("Voter2","Bobby")

voting_system.tally_votes()
voting_system.get_winner()




