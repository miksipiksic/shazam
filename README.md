# shazam

*** Data directory should be added ***

An audio recognition system designed to identify a song cut (a portion of a song) from a given database of songs. The key principles used for this recognition are signal processing techniques, particularly the Fourier transform, which helps in generating a unique fingerprint for each song in the database.

1. Song Fingerprint Generation: To recognize a song, the software first generates a unique fingerprint for each song in the database using signal processing principles, like the Fourier transform. This fingerprint represents the characteristic features of the song's audio data and helps in quick identification.

2. Song Matrix Generation: The software converts each full song and song cut into matrices that represent the audio data in a structured way. These matrices are essential for comparison and matching purposes.

3. Matching Function: This function compares the song cut matrix with each full song matrix in the database. It checks whether the song cut matrix is a submatrix (a smaller part) of the full song matrix. In other words, it verifies if the song cut exists within the full song.

4. Threshold Criteria: The software evaluates whether the matching results meet a specified threshold criterion, usually represented as "max_matches". This threshold is determined through experimentation and indicates the minimum number of matching elements needed to consider a match. If the number of matching elements exceeds this threshold, it's likely that there is a match.

5. Best Match Selection: If multiple songs in the database have matching song cut matrices, the software further evaluates which song has the best score on the matching test. The "best score" refers to the song that has the most significant number of matching elements and meets the threshold criteria (max_matches). This way, the software can identify the song that most accurately matches the provided song cut.
