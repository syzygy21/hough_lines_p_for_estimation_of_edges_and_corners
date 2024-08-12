# hough_lines_p_for_estimation_of_edges_and_corners
The video in the link shows a white piece of paper. For such tasks if we were to compute the corners of the paper then a promising approach is to use the Hough Lines Tranform to detect the straight lines in the image. After, these the intersection points between these lines can be computed which would then give us the corners of the paper.
Pipeline followed in the code:
1. Compute the laplacian of each of the frame in the video to filter out the clear frames in the video for further computation.
2. Take each clear frame from the video and apply computation to detect the edges in the frame.
3. Use the cv2.HoughLinesP method to compute the lines in each frame and also figure out the points of intersection. Use some additional computation to filter out the appropriate points of intersection by considering only those points
   that are closer to the detected lines.
4. (Optional) Utilize certain additional techniques such as the Harris Corner Detection to filter out the appropriate points of intersection by comparing the results from the Hough Lines approach and the Harris Corner approach.
The following image is a snapshot from the result video that can be found at this link.
 <img width="360" alt="result_snapshot" src="https://github.com/user-attachments/assets/80950c79-7630-4cc2-89d1-9ba9f054678a">
The following image shows the result of applying Harris Corner Detection to the video. Refer to the link to to take a look at the full length video of the result of the Harris Corner Detection.
 
