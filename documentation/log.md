# Project Log
## 23/09/2021
1-hour meeting. Discussed the current method under investigation:
1. take input image, turn it into patches
2. use trained GAN to do style transfer on the patches
3. Process ground truth to get the cell markings validation_steps
4. reassemble the patches and count the cells.

Received reading pointers:
   - GANs and Neural Style Transfer (as a specific application, transformation of horses into zebras with CGANs)
   - ImageJ
   - Yolo

Submitted template matching as a possible alternative solution.

## 30/09/2021
No meeting. Continued with reading.

## 07/10/2021
Meeting to clarify the project proposal. Project options discussed:
- Implement a GAN (such as pix2pix) for style transfer of micrographs into computer-interpretable 'binary' images
- Implement a model to count 'cells' in 'binary' images
- Implement a web interface for an existing model

It was clarified that the existing solution is still under development and there is still significant scope for refinement.

## 08/10/2021
Completed & submitted Project Proposal & Ethics Form. Project is to implement a machine learning model for cell counting, not a web interface for such a model.

Feedback on Project Proposal:
- _Citations: the link is fine in the proposal but make sure you cite properly in the actual project document. Use Harvard if you can, but if you're using LaTeX, Vancouver might be easier (it's hard to find a decent Harvard LaTeX bib style)_
- _You're missing the term "semantic segmentation". That's what the "binary" file is - grey for background, black for trichome, white for cell-centre. Semantic segmentation provides a mask showing the "meaning" of each pixel (i.e. which object it belongs to)._
- _You're missing "evaluation of my technique" in your milestones list. I know it'll probably be an iterative approach (develop method, how good is it? Make it better. How good is it now?), but you can mention evaluation of your own model as one of your objectives. AND you can then say that evaluating such a model is a key technique (how do you know your model is any good?)._
- _If you wanted to expand your project plan, you might take a "months and milestones" approach, and you start doing that by looking at your deadlines for the honours project. This will be more important later when you might have to pull yourself out of a research rabbit-hole to make sure you complete the project on time (even if it's not "complete" to the standard you want!)._

Clarification on ethics: the dataset of micrographs is internal to the University and does not create any data protection concerns.

## 14/10/2021
1-hour meeting post-Project Proposal submission. Discussed:
- Labelme
- Grabcut to process rough binary map produced by high pass filter
- Object detection & region proposal in YOLOv5

A possible specification of a project within the bounds of the proposal was suggested: retraining YOLOv5 to _detect_, _localise_, and _count_ cyanobacteria cells.

## 27/10/2021
Feedback received for Project Proposal:

_The project proposal is very thorough and clear. There are a couple of places where I think you could improve. You mention research participants, but that doesn’t necessarily fit in with the rest of the proposal (any more), and you’ve named some key techniques but you could do with slightly more detail on some of them. For example, machine learning can be implemented in many ways, and python libraries like keras or pytorch facilitate this. Your project plan is detailed enough that it will see you complete the project in a timely manner, and the background and motivation sections are excellent. Your writing style is lucid and appropriate for the task._

## 04/11/2021
No meeting. Continued with reading.

## 12/11/2021
Decided to postpone meeting in favour of continuing with Literature Review.

## 15/11/2021
In-person meeting discussing the literature review:
- Follow a 'here's how it was done, here's why it was good, here's how it relates to my  project' approach
- The example literature reviews represent exactly what is required
- Include abstract & table of contents
- Include *applied* references, i.e. those which can be 'tied back' to the project requirements. For example, YOLO has implementations in both Keras and Pytorch. This is a piece of info worth tying back to the project's non-functional requirements. Another could be a comparison of regularisation functions Adam and SGD

## 18/01/2022
30-minute in-person meeting. Revisited the project scope (retrain YOLO on Micropics, repeat if possible) and the state of the project so far (no news).

## 24/01/2022
Began familiarisation with YOLO & micropics repo.

## 25/01/2022
Began critical appraisal of image annotation tools (Labelstudio vs Labelme).
Meeting discussed:
- The process of patching images (if blank patches are to be removed, a new approach will need to be developed since the existing one presumes a processed image with a black background)
- The structure of the final report (Design, Implementation, Evaluation)

## 23/02/2022
In-person meeting. Discussed:
- HOG descriptors
- Transfer learning for retraining YOLO
  - Justify the model used as a basis
- Reducing oscillation (reduce learning rate by factor of 10 or 100)
- The possibility of data processing introducing bias
- Distortion/occlusion/foreshortening of images
- Writing up
  - Write in the order things are done
  - Methodology, Results, and Evaluation are graded separately
  - Read the grading grid
  - Reflection - justify the method used
  - The first and last paragraph of a section, apart from the rest, should make sense
  - If it doesn't correspond to an Aim/Objective, it doesn't count
  - Refer to As&Os in Conclusion

## 26/02/2022
Set up NGX & became familiarised with the system