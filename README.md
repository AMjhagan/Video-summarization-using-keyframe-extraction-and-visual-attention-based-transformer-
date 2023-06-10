# Video summarization using keyframe extraction and visual attention-based transformer     
This project presents a visual-attention transformer based video summarization tool.

# Idea and description
The purpose of this project is convert a video into a textual summary by using key-frame extraction and image captioning. The advantage video summarization is that it is easier to go through text compared to video and text takes less storage space compared to video.

# Steps involved in video summarization
1. Key frame extraction using pixel difference in LUV colourspace
2. Generate caption for each keyframe using transformer
3. Combine the captions and do corrections in the summary using GPT-3

# Key frame extraction using pixel difference in LUV colourspace
Keyframe detection in video processing selects representative frames that capture the essence of a video. These frames exhibit significant visual or semantic changes, like scene transitions or object movements. The selection process involves calculating the sum of absolute pixel differences in the LUV color space, which separates color (UV) from lightness (L) and closely aligns with human perception. This approach improves the accuracy of summarizing video content compared to using the RGB color space.

# Generate caption for each keyframe using transformer
The Transformer is a neural network design known for its exceptional performance in NLP tasks and image captioning. Comprising an encoder, decoder, and cross-attention module, it borrows its name from a fictional robot. The encoder, a pre-trained CNN, extracts visual attributes from input images. The decoder, based on the Transformer, generates descriptive captions by combining visual elements and textual information. The cross-attention module enables simultaneous consideration of visual and textual data, resulting in informative and coherent captions.

# Combine the captions and do corrections in the summary using GPT-3
Finally, all the individual captions corresponding to each image are combined together to form a paragraph. GPT-3 is then used to make grammatical and logical errors in the final paragraph.

# Dataset used
Flicker30k dataset
https://www.kaggle.com/datasets/eeshawn/flickr30k
This dataset consists of 30,000 images and 5 sentences describing each image.
