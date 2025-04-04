# Awesome Controllabe Speech Synthesis

This is an evolving repo for the survey: [Towards Controllable Speech Synthesis in the Era of Large Language Models: A Survey](https://arxiv.org/abs/2412.06602). If you find our survey useful for your research, please 📚cite📚 the following paper:

```latex
@article{xie2024towards,
  title={Towards Controllable Speech Synthesis in the Era of Large Language Models: A Survey},
  author={Xie, Tianxin and Rong, Yan and Zhang, Pengfei and Liu, Li},
  journal={arXiv preprint arXiv:2412.06602},
  year={2024}
}
```

<p align="center">
    <img src="./images/sec1_summary.jpg" width="1000"/>
</p>
<p align="center">
    <img src="./images/sec2_pipeline.jpg" width="1000"/>
</p>
<p align="center">
    <img src="./images/sec5_control_strategies.jpg" width="1000"/>
</p>
<p align="center">
<img src="./images/sec6_challenges.jpg" width="500"/>
</p>

## 🚀 Non-autoregressive Controllable TTS

Below are representative non-autoregressive controllable TTS methods. Each entry follows this format: **method name, zero-shot capability, controllability, acoustic model, vocoder, acoustic feature, release date, and code/demo/checkpoint**.

- [FastSpeech](https://proceedings.neurips.cc/paper_files/paper/2019/hash/f63f65b503e22cb970527f23c9ad7db1-Abstract.html), Zero-shot (✗), Controllability (Speed, Prosody), Transformer, [WaveGlow](https://github.com/NVIDIA/waveglow), MelS, 2019.05, [Code (unofficial)](https://github.com/xcmyz/FastSpeech)
- [FastSpeech 2](https://arxiv.org/abs/2006.04558), Zero-shot (✗), Controllability (Pitch, Energy, Speed, Prosody), Transformer, [Parallel WaveGAN](https://github.com/kan-bayashi/ParallelWaveGAN), MelS, 2020.06, [Code (unofficial)](https://github.com/ming024/FastSpeech2)
- [FastPitch](https://ieeexplore.ieee.org/abstract/document/9413889), Zero-shot (✗), Controllability (Pitch, Prosody), Transformer, [WaveGlow](https://github.com/NVIDIA/waveglow), MelS, 2020.06, [Code](https://github.com/NVIDIA/DeepLearningExamples/tree/master/PyTorch/SpeechSynthesis/FastPitch)
- [Parallel Tacotron](https://ieeexplore.ieee.org/abstract/document/9414718), Zero-shot (✗), Controllability (Prosody), Transformer + CNN, [WaveRNN](https://github.com/fatchord/WaveRNN), MelS, 2020.10, [Demo](https://google.github.io/tacotron/publications/parallel_tacotron/)
- [StyleTagging-TTS](https://arxiv.org/abs/2104.00436), Zero-shot (✓), Controllability (Timbre, Emotion), Transformer + CNN, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2021.04, [Demo](https://gannnn123.github.io/styletaggingtts-demo/)
- [SC-GlowTTS](https://arxiv.org/abs/2104.05557), Zero-shot (✓), Controllability (Timbre), Transformer + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2021.06, [Demo](https://edresson.github.io/SC-GlowTTS/), [Code](https://github.com/Edresson/SC-GlowTTS)
- [Meta-StyleSpeech](https://proceedings.mlr.press/v139/min21b.html), Zero-shot (✓), Controllability (Timbre), Transformer, [MelGAN](https://arxiv.org/abs/1910.06711), MelS, 2021.06, [Code](https://github.com/KevinMIN95/StyleSpeech)
- [DelightfulTTS](https://arxiv.org/abs/2110.12612), Zero-shot (✗), Controllability (Pitch, Speed, Prosody), Transformer + CNN, [HiFiNet](https://github.com/yl4579/HiFTNet), MelS, 2021.11, [Demo](https://cognitivespeech.github.io/delightfultts)
- [YourTTS](https://proceedings.mlr.press/v162/casanova22a.html), Zero-shot (✓), Controllability (Timbre), Transformer + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), LinS, 2021.12, [Demo & Checkpoint](https://github.com/Edresson/YourTTS)
- [StyleTTS](https://arxiv.org/abs/2205.15439), Zero-shot (✓), Controllability (Timbre), CNN + RNN, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2022.05, [Code](https://github.com/yl4579/StyleTTS)
- [GenerSpeech](https://proceedings.neurips.cc/paper_files/paper/2022/hash/4730d10b22261faa9a95ebf7497bc556-Abstract-Conference.html), Zero-shot (✓), Controllability (Timbre), Transformer + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2022.05, [Demo](https://generspeech.github.io/)
- [Cauliflow](https://arxiv.org/abs/2206.14165), Zero-shot (✗), Controllability (Speed, Prosody), BERT + Flow, [UP WaveNet](https://arxiv.org/abs/2102.01106), MelS, 2022.06
- [CLONE](https://arxiv.org/abs/2207.06088), Zero-shot (✗), Controllability (Pitch, Speed, Prosody), Transformer + CNN, [WaveNet](https://arxiv.org/abs/1609.03499), MelS + LinS, 2022.07, [Demo](https://xcmyz.github.io/CLONE/)
- [PromptTTS](https://ieeexplore.ieee.org/abstract/document/10096285), Zero-shot (✗), Controllability (Pitch, Energy, Speed, Prosody, Timbre, Emotion, Description), Bert + Transformer, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2022.11, [Demo](https://speechresearch.github.io/prompttts/)
- [Grad-StyleSpeech](https://ieeexplore.ieee.org/abstract/document/10095515), Zero-shot (✓), Controllability (Timbre), Score-based Diffusion, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2022.11, [Demo](https://nardien.github.io/grad-stylespeech-demo/)
- [NaturalSpeech 2](https://arxiv.org/abs/2304.09116), Zero-shot (✓), Controllability (Timbre), Diffusion, [RVQ-based Codec](https://arxiv.org/abs/2304.09116), Token, 2023.04, [Demo](https://speechresearch.github.io/naturalspeech2/), [Code (unofficial)](https://github.com/lucidrains/naturalspeech2-pytorch)
- [PromptStyle](https://arxiv.org/abs/2305.19522), Zero-shot (✓), Controllability (Pitch, Prosody, Timbre, Emotion, Description), [VITS](https://arxiv.org/abs/2106.06103) + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.05, [Demo](https://promptstyle.github.io/PromptStyle)
- [StyleTTS 2](https://proceedings.neurips.cc/paper_files/paper/2023/hash/3eaad2a0b62b5ed7a2e66c2188bb1449-Abstract-Conference.html), Zero-shot (✓), Controllability (Prosody, Timbre, Emotion), Flow-based Diffusion + GAN, [HiFi-GAN](https://github.com/jik876/hifi-gan) / [iSTFTNet](https://github.com/rishikksh20/iSTFTNet-pytorch), MelS, 2023.06
- [VoiceBox](https://proceedings.neurips.cc/paper_files/paper/2023/hash/2d8911db9ecedf866015091b28946e15-Abstract-Conference.html), Zero-shot (✓), Controllability (Timbre), Transformer + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.06, [Demo](https://voicebox.metademolab.com/), [Code (unofficial)](https://github.com/lucidrains/voicebox-pytorch)
- [MegaTTS 2](https://openreview.net/forum?id=mvMI3N4AvD), Zero-shot (✓), Controllability (Prosody, Timbre, Emotion), Decoder-only Transformer + GAN, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.07, [Demo](https://boostprompt.github.io/boostprompt/), [Code (unofficial)](https://github.com/LSimon95/megatts2)
- [PromptTTS 2](https://arxiv.org/abs/2309.02285), Zero-shot (✗), Controllability (Pitch, Energy, Speed, Prosody, Timbre, Description), Diffusion, [RVQ-based Codec]((https://arxiv.org/abs/2309.02285)), Latent Feature, 2023.09, [Demo](https://speechresearch.github.io/prompttts2/)
- [VoiceLDM](https://ieeexplore.ieee.org/abstract/document/10448268), Zero-shot (✗), Controllability (Pitch, Prosody, Timbre, Emotion, Environment, Description), Diffusion, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.09, [Demo](https://voiceldm.github.io/), [Code](https://github.com/glory20h/VoiceLDM)
- [DuIAN-E](https://arxiv.org/abs/2309.12792), Zero-shot (✗), Controllability (Pitch, Speed, Prosody), CNN + RNN, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.09, [Demo](https://sounddemos.github.io/durian-e/)
- [PromptTTS++](https://ieeexplore.ieee.org/abstract/document/10448173), Zero-shot (✗), Controllability (Pitch, Speed, Prosody, Timbre, Emotion, Description), Transformer + Diffusion, [BigVGAN](https://github.com/NVIDIA/BigVGAN), MelS, 2023.09, [Demo](https://reppy4620.github.io/demo.promptttspp/), [Code](https://github.com/line/promptttspp)
- [SpeechFlow](https://arxiv.org/abs/2310.16338), Zero-shot (✓), Controllability (Timbre), Transformer + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.10, [Demo](https://voicebox.metademolab.com/speechflow.html)
- [P-Flow](https://proceedings.neurips.cc/paper_files/paper/2023/hash/eb0965da1d2cb3fbbbb8dbbad5fa0bfc-Abstract-Conference.html), Zero-shot (✓), Controllability (Timbre), Transformer + Flow, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2023.10, [Demo](https://research.nvidia.com/labs/adlr/projects/pflow/), [Code (unofficial)](https://github.com/p0p4k/pflowtts_pytorch)
- [E3 TTS](https://ieeexplore.ieee.org/abstract/document/10389766), Zero-shot (✓), Controllability (Timbre), Diffusion, Not required, Waveform, 2023.11, [Demo](https://e3tts.github.io/)
- [HierSpeech++](https://arxiv.org/abs/2311.12454), Zero-shot (✓), Controllability (Timbre), Transformer + VAE + Flow, [BigVGAN](https://github.com/NVIDIA/BigVGAN), MelS, 2023.11, [Demo](https://sh-lee-prml.github.io/HierSpeechpp-demo/), [Code](https://github.com/sh-lee-prml/HierSpeechpp)
- [Audiobox](https://arxiv.org/abs/2312.15821), Zero-shot (✓), Controllability (Pitch, Speed, Prosody, Timbre, Environment, Description), Transformer + Flow, [EnCodec](https://github.com/facebookresearch/encodec), MelS, 2023.12, [Demo](https://audiobox.metademolab.com/)
- [FlashSpeech](https://dl.acm.org/doi/abs/10.1145/3664647.3681044), Zero-shot (✓), Controllability (Timbre), Latent Consistency Model, [EnCodec](https://github.com/facebookresearch/encodec), Token, 2024.04, [Demo](https://flashspeech.github.io/), [Code](https://github.com/zhenye234/FlashSpeech)
- [NaturalSpeech 3](https://arxiv.org/abs/2403.03100), Zero-shot (✓), Controllability (Speed, Prosody, Timbre), Transformer + Diffusion, [FACodec](https://github.com/lifeiteng/naturalspeech3_facodec), Token, 2024.04, [Demo](https://speechresearch.github.io/naturalspeech3/)
- [InstructTTS](https://ieeexplore.ieee.org/abstract/document/10534832), Zero-shot (✗), Controllability (Pitch, Speed, Prosody, Timbre, Emotion, Description), Transformer + Diffusion, [HiFi-GAN](https://github.com/jik876/hifi-gan), Token, 2024.05, [Demo](https://dongchaoyang.top/InstructTTS/)
- [ControlSpeech](https://arxiv.org/abs/2406.01205), Zero-shot (✓), Controllability (Pitch, Energy, Speed, Prosody, Timbre, Emotion, Description), Transformer + Diffusion, [FACodec](https://github.com/lifeiteng/naturalspeech3_facodec), Token, 2024.06, [Demo](https://controlspeech.github.io/), [Code](https://github.com/jishengpeng/ControlSpeech)
- [AST-LDM](https://arxiv.org/abs/2406.12688), Zero-shot (✗), Controllability (Timbre, Environment, Description), Diffusion + VAE, [HiFi-GAN](https://github.com/jik876/hifi-gan), MelS, 2024.06, [Demo](https://ast-ldm.github.io/demo/)
- [SimpleSpeech](https://arxiv.org/abs/2406.02328), Zero-shot (✓), Controllability (Timbre), Transformer + Diffusion, [SQ Codec](https://arxiv.org/abs/2406.02328), Token, 2024.06, [Demo](https://simplespeech.github.io/simplespeechDemo/), [Code](https://github.com/yangdongchao/SimpleSpeech)

|Method|ZS|Pit.|Ene.|Spe.|Pro.|Tim.|Emo.|Env.|Des.|Acoustic<br>Model|Vocoder|Acoustic<br>Feature|Release<br>Time|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|[DiTTo-TTS](https://arxiv.org/abs/2406.11427)|✓|||✓||✓||||DiT|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|Token|2024.06|
|[E2 TTS](https://arxiv.org/abs/2406.18009)|✓|||||✓||||Flow Matching Transformer|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|MelS|2024.06|
|[MobileSpeech](https://arxiv.org/abs/2402.09378)|✓|||||✓||||ConFormer Decoder|Vocos|Token|2024.06|
|[DEX-TTS](https://arxiv.org/abs/2406.19135)|✓|||||✓||||Diffusion|[HiFi-GAN](https://github.com/jik876/hifi-gan)|MelS|2024.06|
|[ArtSpeech](https://dl.acm.org/doi/abs/10.1145/3664647.3681097)|✓|||||✓||||RNN + CNN|[HiFI-GAN](https://github.com/jik876/hifi-gan)|MelS|2024.07|
|[CCSP](https://dl.acm.org/doi/abs/10.1145/3664647.3681348)|✓|||||✓||||Diffusion|Codec Decoder|Token|2024.07|
|[SimpleSpeech 2](https://arxiv.org/abs/2408.13893)|✓|||✓||✓||||Flow-based Transformer Diffusion|SQ Decoder|Token|2024.08|
|[E1 TTS](https://arxiv.org/abs/2409.09351)|✓|||||✓||||DiT|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|Token|2024.09|
|[VoiceGuider](https://arxiv.org/abs/2409.15759)|✓|||||✓||||Diffusion|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|MelS|2024.09|
|[StyleTTS-ZS](https://arxiv.org/abs/2409.10058)|✓|||||✓||||Diffusion + GAN|HifiGAN / iSTFTNet|Token|2024.09|
|[NansyTTS](https://arxiv.org/abs/2409.17452)|✓|✓||✓|✓|✓|||✓|Transformer|NANSY++|MelS|2024.09|
|[NanoVoice](https://arxiv.org/abs/2409.15760)|✓|||||✓||||Diffusion|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|MelS|2024.09|
|[MS$^{2}$KU-VTTS](https://arxiv.org/abs/2410.14101)||||||||✓|✓|Diffusion|[BigvGAN](https://github.com/NVIDIA/BigVGAN)|MelS|2024.10|
|[MaskGCT](https://arxiv.org/abs/2409.00750)|✓|||✓||✓||||Masked Generative Transformers|DAC + Vocos|Token|2024.10|

*Abbreviations*: Z(ero-)S(hot), Pit(ch), Ene(rgy)=Volume, Spe(ed), Pro(sody), Tim(bre), Emo(tion), Env(ironment), Des(cription). Timbre involves gender and age. MelS and LinS represent Mel Spectrogram and Linear Spectrogram, respectively.

## 🎞️ Autoregressive Controllable TTS

|Method|ZS|Pit.|Ene.|Spe.|Pro.|Tim.|Emo.|Env.|Des.|Acoustic<br>Model|Vocoder|Acoustic<br>Feature|Release<br>Time|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|[Prosody-Tacotron](https://proceedings.mlr.press/v80/skerry-ryan18a.html)||✓|||✓|||||RNN|WaveNet|MelS|2018.03|
|[GST-Tacotron](https://ieeexplore.ieee.org/abstract/document/8639682)||✓|||✓|||||CNN + RNN|Griffin-Lim|LinS|2018.03|
|[GMVAE-Tacotron](https://arxiv.org/abs/1810.07217)||✓||✓|✓|||✓||CNN + RNN|WaveRNN|MelS|2018.12|
|[VAE-Tacotron](https://ieeexplore.ieee.org/abstract/document/8683623)||✓||✓|✓|||||CNN + RNN|WaveNet|MelS|2019.02|
|[DurIAN](https://arxiv.org/abs/1909.01700)||✓||✓|✓|||||CNN + RNN|MB-WaveRNN|MelS|2019.09|
|[Flowtron](https://arxiv.org/abs/2005.05957)||✓||✓|✓|||||CNN + RNN|[WaveGlow](https://github.com/NVIDIA/waveglow)|MelS|2020.07|
|[MsEmoTTS](https://ieeexplore.ieee.org/abstract/document/9693186)||✓|||✓||✓|||CNN + RNN|WaveRNN|MelS|2022.01|
|[VALL-E](https://arxiv.org/abs/2301.02111)|✓|||||✓||||LLM|[EnCodec](https://github.com/facebookresearch/encodec)|Token|2023.01|
|[SpearTTS](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00618/118854)|✓|||||✓||||LLM|SoundStream|Token|2023.02|
|[VALL-E X](https://arxiv.org/abs/2303.03926)|✓|||||✓||||LLM|[EnCodec](https://github.com/facebookresearch/encodec)|Token|2023.03|
|[Make-a-voice](https://arxiv.org/abs/2305.19269)|✓|||||✓||||LLM|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|Token|2023.05|
|[TorToise](https://arxiv.org/abs/2305.07243)||||||✓||||Transformer + DDPM|Univnet|MelS|2023.05|
|[MegaTTS](https://arxiv.org/abs/2306.03509)|✓|||||✓||||LLM + GAN|[HiFi-GAN](https://github.com/jik876/hifi-gan)|MelS|2023.06|
|[SC VALL-E](https://arxiv.org/abs/2307.10550)|✓|✓||✓|✓|✓|✓|||LLM|[EnCodec](https://github.com/facebookresearch/encodec)|Token|2023.07|
|[Salle](https://ieeexplore.ieee.org/abstract/document/10445879)||✓|✓|✓|✓|✓|✓||✓|LLM|Codec Decoder|Token|2023.08|
|[UniAudio](https://arxiv.org/abs/2310.00704)|✓|✓||✓|✓|✓|||✓|LLM|[EnCodec](https://github.com/facebookresearch/encodec)|Token|2023.10|
|[ELLA-V](https://arxiv.org/abs/2401.07333)|✓|||||✓||||LLM|[EnCodec](https://github.com/facebookresearch/encodec)|Token|2024.01|
|[BaseTTS](https://arxiv.org/abs/2402.08093)|✓|||||✓||||LLM|UnivNet|Token|2024.02|
|[ClaM-TTS](https://arxiv.org/abs/2404.02781)|✓|||||✓||||LLM|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|MelS+Token|2024.04|
|[RALL-E](https://arxiv.org/abs/2404.03204)|✓|||||✓||||LLM|SoundStream|Token|2024.05|
|[ARDiT](https://arxiv.org/abs/2406.05551)|✓|||✓||✓||||Decoder-only Diffusion Transformer|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|MelS|2024.06|
|[VALL-E R](https://arxiv.org/abs/2406.07855)|✓|||||✓||||LLM|Vocos|Token|2024.06|
|[VALL-E 2](https://arxiv.org/abs/2406.05370)|✓|||||✓||||LLM|Vocos|Token|2024.06|
|[Seed-TTS](https://arxiv.org/abs/2406.02430)|✓|||||✓|✓|||LLM + Diffusion Transformer|/|Token|2024.06|
|[VoiceCraft](https://arxiv.org/abs/2403.16973)|✓|||||✓||||LLM|[HiFi-GAN](https://github.com/jik876/hifi-gan)|Token|2024.06|
|[XTTS](https://arxiv.org/abs/2406.04904)|✓|||||✓||||LLM + GAN|[HiFi-GAN](https://github.com/jik876/hifi-gan)|MelS+Token|2024.06|
|[CosyVoice](https://arxiv.org/abs/2407.05407)|✓|✓||✓|✓|✓|✓||✓|LLM + Conditional Flow Matching|[HiFi-GAN](https://github.com/jik876/hifi-gan)|Token|2024.07|
|[MELLE](https://arxiv.org/abs/2407.08551)|✓|||||✓||||LLM|[HiFi-GAN](https://github.com/jik876/hifi-gan)|MelS|2024.07|
|[Bailing TTS](https://arxiv.org/abs/2408.00284)|✓|||||✓||||LLM + Diffusion Transformer|/|Token|2024.08|
|[VoxInstruct](https://dl.acm.org/doi/abs/10.1145/3664647.3681680)|✓|✓|✓|✓|✓|✓|✓||✓|LLM|Vocos|Token|2024.08|
|[Emo-DPO](https://arxiv.org/abs/2409.10157)|||||||✓||✓|LLM|[HiFi-GAN](https://github.com/jik876/hifi-gan)|Token|2024.09|
|[FireRedTTS](https://arxiv.org/abs/2409.03283)|✓||||✓|✓||||LLM + Conditional Flow Matching|[BigVGAN](https://github.com/NVIDIA/BigVGAN)-v2|Token|2024.09|
|[CoFi-Speech](https://arxiv.org/abs/2409.11630)|✓|||||✓||||LLM|[BigVGAN](https://github.com/NVIDIA/BigVGAN)|Token|2024.09|
|[Takin](https://arxiv.org/abs/2409.12139)|✓|✓||✓|✓|✓|✓||✓|LLM|HiFi-Codec|Token|2024.09|
|[HALL-E](https://arxiv.org/abs/2410.04380)|✓|||||✓||||LLM|[EnCodec](https://github.com/facebookresearch/encodec)|Token|2024.10|

*Abbreviations*: Z(ero-)S(hot), Pit(ch), Ene(rgy)=Volume, Spe(ed), Pro(sody), Tim(bre), Emo(tion), Env(ironment), Des(cription). Timbre involves gender and age. MelS and LinS represent Mel Spectrogram and Linear Spectrogram, respectively.

## 💾 Datsets

A summary of open-source datasets for controllable TTS:

|Dataset|Hours|#Speakers|Labels||||||||||||Lang|Release<br>Time|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
||||Pit.|Ene.|Spe.|Age|Gen.|Emo.|Emp.|Acc.|Top.|Des.|Env.|Dia.|||
|[Taskmaster-1](https://arxiv.org/abs/1909.05358)|/|/||||||||||||✓|en|2019.09|
|[Libri-light](https://ieeexplore.ieee.org/abstract/document/9052942)|60,000|9,722|||||||||✓||||en|2019.12|
|[AISHELL-3](https://arxiv.org/abs/2010.11567)|85|218||||✓|✓|||✓|||||zh|2020.10|
|[ESD](https://www.sciencedirect.com/science/article/pii/S0167639321001308)|29|10||||||✓|||||||en,zh|2021.05|
|[GigaSpeech](https://arxiv.org/abs/2106.06909)|10,000|/|||||||||✓||||en|2021.06|
|[WenetSpeech](https://ieeexplore.ieee.org/abstract/document/9746682)|10,000|/|||||||||✓||||zh|2021.07|
|[PromptSpeech](https://ieeexplore.ieee.org/abstract/document/10096285)|/|/|✓|✓|✓|||✓||||✓|||en|2022.11|
|[DailyTalk](https://ieeexplore.ieee.org/abstract/document/10095751)|20|2||||||✓|||✓|||✓|en|2023.05|
|[TextrolSpeech](https://ieeexplore.ieee.org/abstract/document/10445879)|330|1,324|✓|✓|✓||✓|✓||||✓|||en|2023.08|
|[VoiceLDM](https://ieeexplore.ieee.org/abstract/document/10448268)|/|/|✓||||✓|✓||||✓|✓||en|2023.09|
|[VccmDataset](https://arxiv.org/abs/2406.01205)|330|1,324|✓|✓|✓||✓|✓||||✓|||en|2024.06|
|[MSceneSpeech](https://arxiv.org/abs/2407.14006)|13|13|||||||||✓||||zh|2024.07|
|[SpeechCraft](https://dl.acm.org/doi/abs/10.1145/3664647.3681674)|2,391|3,200|✓|✓|✓|✓|✓|✓|✓||✓|✓|||en,zh|2024.08|

*Abbreviations*: Pit(ch), Ene(rgy)=volume=loudness, Spe(ed)=duration, Gen(der), Emo(tion), Emp(hasis), Acc(ent), Dia(logue), Env(ironment), Des(cription).

## 📏 Evaluation Metrics

| Metric | Type | Eval Target | GT Required |
|:---:|:---:|:---:|:---:|
| Mel-Cepstral Distortion (MCD) $\downarrow$ | Objective | Acoustic similarity | ✓ |
| Frequency Domain Score Difference (FDSD) $\downarrow$ | Objective | Acoustic similarity | ✓ |
| Word Error Rate (WER) $\downarrow$ | Objective | Intelligibility | ✓ |
| Cosine Similarity $\downarrow$ | Objective | Speaker similarity | ✓ |
| Perceptual Evaluation of Speech Quality (PESQ) $\uparrow$ | Objective | Perceptual quality | ✓ |
| Signal-to-Noise Ratio (SNR) $\uparrow$ | Objective | Perceptual quality | ✓ |
| Mean Opinion Score (MOS) $\uparrow$ | Subjective | Preference | |
| Comparison Mean Opinion Score (CMOS) $\uparrow$ | Subjective | Preference | |
| AB Test | Subjective | Preference | |
| ABX Test | Subjective | Perceptual similarity | ✓ |

GT: Ground truth, $\downarrow$: Lower is better, $\uparrow$: Higher is better.
