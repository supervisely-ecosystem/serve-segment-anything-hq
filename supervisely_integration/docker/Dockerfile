FROM supervisely/base-py-sdk:6.72.111
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update

RUN pip3 install torch==1.12.1+cu113 --extra-index-url https://download.pytorch.org/whl/cu113
RUN pip3 install torchvision==0.13.1+cu113 --extra-index-url https://download.pytorch.org/whl/cu113
RUN pip3 install cachetools
RUN pip3 install timm==0.4.9

RUN python3 -m pip install supervisely==6.72.137

RUN mkdir -p weights
RUN wget https://huggingface.co/lkeab/hq-sam/resolve/main/sam_hq_vit_tiny.pth -O /weights/vit_tiny_sam_hq.pth
RUN wget https://huggingface.co/lkeab/hq-sam/resolve/main/sam_hq_vit_b.pth -O /weights/vit_b_sam_hq.pth
RUN wget https://huggingface.co/lkeab/hq-sam/resolve/main/sam_hq_vit_l.pth -O /weights/vit_l_sam_hq.pth
RUN wget https://huggingface.co/lkeab/hq-sam/resolve/main/sam_hq_vit_h.pth -O /weights/vit_h_sam_hq.pth
