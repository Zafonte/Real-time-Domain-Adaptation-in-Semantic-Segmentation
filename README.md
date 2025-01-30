# AML-project
Real-time Domain Adaptation in  Semantic Segmentation project developed for the Advanced Machine Learning course at the Polytechnic of Turin.

This work was done by:
* Della Croce Andrea
* Terramagra Federica
* Zafonte Francesca

Link to download the Utils folder, in case the automatic download doesn't work: https://drive.google.com/drive/folders/1-JDJJW2axscgz6x7mzVmS_kxozavkb0L?usp=sharing

# Repository Structure

This repository contains various solutions and experiments for semantic segmentation tasks, domain shift evaluation, and unsupervised domain adaptation (UDA). Below is an overview of its structure:

## Semantic Segmentation
This section includes solutions for semantic segmentation tasks, both classic and real-time, on the **LoveDA dataset**.

- **deeplab_v2**: A solution for the classic semantic segmentation task.
- **pidnet**: A solution for real-time semantic segmentation.

## Domain Shift
This section addresses the domain shift problem in semantic segmentation, specifically evaluating the performance of models trained on the **Urban** source domain and tested on the **Rural** target domain. The models are trained and evaluated with different resolutions and batch sizes.

- **256_16**
  - **pidnet_Uban_to_Rural_256_16**: Model trained on the Urban source domain and applied to the Rural target domain, using a resolution of 256x256 and a batch size of 16.
  
- **512_16**
  - **pidnet_Uban_to_Rural_512_16**: Model trained on the Urban source domain and applied to the Rural target domain, using a resolution of 512x512 and a batch size of 16.
  
- **512_32**
  - **pidnet_Uban_to_Rural_512_32**: Model trained on the Urban source domain and applied to the Rural target domain, using a resolution of 512x512 and a batch size of 32.
  - **pidnet_Uban_to_Rural_512_32_wHF**: Application of data augmentation (with Histogram-based Filtering) to reduce domain shift, using a resolution of 512x512 and a batch size of 32.

## Unsupervised Domain Adaptation (UDA)
This section explores techniques to mitigate domain shift through unsupervised domain adaptation methods.

- **adversarial_approach**: The application of an adversarial UDA technique to reduce domain shift.
- **image_to_image_approach**: The application of an image-to-image UDA technique to reduce domain shift.

## Extensions
This section includes experiments that explore the use of alternative segmentation losses to address class distribution inconsistencies and hyperparameter tuning.

- **image_to_image_optWL**: Use of an optimized weighted loss function.
- **image_to_image_optWL_multiStepLR**: Use of a weighted loss function with multi-step learning rate decay.
- **image_to_image_optFocalLoss_multiStepLR**: Application of Focal Loss with multi-step learning rate decay.
- **image_to_image_optWeightedFocalLoss_multiStepLR**: Use of a weighted Focal Loss function with multi-step learning rate decay.
- **adversarial_approach_optWL_multiStepLR_polylr**: Adversarial approach with weighted loss and multi-step learning rate decay using polynomial learning rate scheduling.
- **pidnet_Uban_to_Rural_512_32_wHF_optWL**: Domain shift model with Histogram-based Filtering and an optimized weighted loss.
- **pidnet_Uban_to_Rural_512_32_wHF_FocalLoss_MultiStepLR**: Domain shift model with Histogram-based Filtering, Focal Loss, and multi-step learning rate decay.
- **pidnet_Uban_to_Rural_512_32_wHF_weightedLoss_MultiStepLR**: Domain shift model with Histogram-based Filtering, weighted loss, and multi-step learning rate decay.

---

This repository provides a comprehensive framework for addressing domain shift in semantic segmentation tasks and experimenting with various domain adaptation and loss function techniques.



