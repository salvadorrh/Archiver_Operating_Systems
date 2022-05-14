# Video Player code 

This is the code I added to create the Video Player. This Video Player transforms a given video clip into a grayscale version. It will consists of the same video, except that it will be in black and white, instead of a color version video.

To do this I used the Producer Consumer Algorithm which will make this project work in parallel and therefore faster to execute.

Note that the Producer Consumer Algorithm is needed with two queues. The first queue will contain the frames that are taken from the original video, which will be transformed into grayscale frames. The second queue will have the frames that are in a grayscale format which will be later on taken and displayed as the new video.

Producer Consumer is needed for two reasons:
When you want to move one frame from one queue to the other, it's important that the 2nd queue (the consumer) should have an empty space for the producer to produce into. If not there will problems.
When you want the 2nd queue to consume, it is needed for the producer to have one frame already produced for the consumer to consume.

Synchronization is vital. If not done carefully, we can get into a deadlock.
