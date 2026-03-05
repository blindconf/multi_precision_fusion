# Adversarial example demo

Supplementary material containing a selection of benign, adversarial, and noisy data employed in our [*paper*](https://arxiv.org/abs/2305.17000).

For each sample, we include the word error rate (WER) or the character error rate (CER) as an accuracy metric and the segmental signal-to-noise ratio (SNR<sub>seg</sub>) as a quality noise metric.
An SNR<sub>seg</sub> exceeding 0 dB indicates a stronger signal presence compared to noise. 
These samples are sourced from the [*Librispeech*](https://www.openslr.org/12), [*Commonvoice*](https://commonvoice.mozilla.org/en), and [*Aishell*](https://www.openslr.org/33/) corpus datasets.

## Librispeech - English
###### Sample 1 
<pre>Benign transcription:       <em>THEN HE LOOKED DOWN THE LAGOON WAS DRY</em>
Adversarial transcription:  <em>PEARL WAS A BORN OUTCAST OF THE INFANTILE WORLD</em>
</pre> &nbsp;
[**benign**: *WER*=0.00],               [**noisy**: *WER*=62.50, SNR<sub>seg</sub>=-4.79]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/1995-1837-0013_benign.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/1995-1837-0013_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *WER*=0.00, SNR<sub>seg</sub>=24.50],   [**psychoacoustic**: *WER*=0.00, SNR<sub>seg</sub>=25.36]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/1995-1837-0013_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/1995-1837-0013_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *WER*=0.00, SNR<sub>seg</sub>=-0.60]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/1995-1837-0013_gc.wav" type="audio/wav" />
</audio>

###### Sample 2 
<pre>Benign transcription:       <em>HOW JOLLY IT WAS BEING YOUNG HILDA</em>
Adversarial transcription:  <em>THERE WAS A GRIM SMILE OF AMUSEMENT ON HIS SHREWD FACE</em>
</pre> &nbsp;
[**benign**: *WER*=0.00],               [**noisy**: *WER*=0.00, SNR<sub>seg</sub>=6.03]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/4446-2273-0017_benign.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/4446-2273-0017_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *WER*=0.00, SNR<sub>seg</sub>=22.04],   [**psychoacoustic**: *WER*=0.00, SNR<sub>seg</sub>=22.95]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/4446-2273-0017_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/4446-2273-0017_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *WER*=0.00, SNR<sub>seg</sub>=-5.87]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Librispeech/4446-2273-0017_gc.wav" type="audio/wav" />
</audio>


## Common Voice v.6 - German

###### Sample 1 
<pre>Benign transcription:       <em>DAS HAT SCHON MEINE URGROßMUTTER GESAGT</em>
Adversarial transcription:  <em>NEU DELHI IST DIE HAUPTSTADT VON INDIEN</em>
</pre> &nbsp;
[**benign**: *WER*=0.00],               [**noisy**: *WER*=0.00, SNR<sub>seg</sub>=-20.24]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_17914813_benign.mp3" type="audio/mp3" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_17914813_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *WER*=0.00, SNR<sub>seg</sub>=9.05],   [**psychoacoustic**: *WER*=0.00, SNR<sub>seg</sub>=11.72]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_17914813_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_17914813_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *WER*=0.00, SNR<sub>seg</sub>=-25.41]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_17914813_gc.wav" type="audio/wav" />
</audio>


###### Sample 2 
<pre>Benign transcription:       <em>ICH GLAUBE ES AUCH NICHT</em>
Adversarial transcription:  <em>WAS SOLLS ICH BIN BEREIT</em>
</pre> &nbsp;
[**benign**: *WER*=0.00],               [**noisy**: *WER*=20.00, SNR<sub>seg</sub>=-17.16]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_18217625_benign.mp3" type="audio/mp3" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_18217625_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *WER*=0.00, SNR<sub>seg</sub>=8.86],   [**psychoacoustic**: *WER*=0.00, SNR<sub>seg</sub>=11.23]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_18217625_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_18217625_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *WER*=0.00, SNR<sub>seg</sub>=-12.88]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/German/common_voice_de_18217625_gc.wav" type="audio/wav" />
</audio>

## Common Voice v.6 - Italian

###### Sample 1 
<pre>Benign transcription:       <em>BERNARDO FALQUI PES</em>
Adversarial transcription:  <em>SEMPRE CARO MI FU QUEST'ERMO COLLE</em>
</pre> &nbsp;
[**benign**: *WER*=66.67],               [**noisy**: *WER*=66.67, SNR<sub>seg</sub>=-3.39]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20088717_benign.mp3" type="audio/mp3" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20088717_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *WER*=0.00, SNR<sub>seg</sub>=10.36],   [**psychoacoustic**: *WER*=0.00, SNR<sub>seg</sub>=13.67]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20088717_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20088717_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *WER*=0.00, SNR<sub>seg</sub>=-12.54]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20088717_gc.wav" type="audio/wav" />
</audio>

###### Sample 2 
<pre>Benign transcription:       <em>PER ESSA È CONSIGLIATA UNA DURATA DI DUE SETTIMANE</em>
Adversarial transcription:  <em>LA LORO PRESENZA ERA PARTICOLARMENTE APPREZZATA DAL PASSEGGERI</em>
</pre> &nbsp;
[**benign**: *WER*=0.00],               [**noisy**: *WER*=55.56, SNR<sub>seg</sub>=-11.31]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20020291_benign.mp3" type="audio/mp3" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20020291_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *WER*=0.00, SNR<sub>seg</sub>=16.05],   [**psychoacoustic**: *WER*=0.00, SNR<sub>seg</sub>=18.96]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20020291_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20020291_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *WER*=0.00, SNR<sub>seg</sub>=-6.73]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/CommonVoice/Italian/common_voice_it_20020291_gc.wav" type="audio/wav" />
</audio>

## Aishell - Mandarin

###### Sample 1 
<pre>Benign transcription:       <em>有 黑客 在 网络 上 兜售 车主 信</em>
Adversarial transcription:  <em>顶级 田径 赛事 再次 落户 鸟巢</em>
</pre> &nbsp;
[**benign**: *CER*=0.00],               [**noisy**: *CER*=0.00, SNR<sub>seg</sub>=6.95]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0908W0304_benign.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0908W0304_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *CER*=0.00, SNR<sub>seg</sub>=21.39],   [**psychoacoustic**: *CER*=0.00, SNR<sub>seg</sub>=25.20]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0908W0304_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0908W0304_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *CER*=0.00, SNR<sub>seg</sub>=-5.87]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0908W0304_gc.wav" type="audio/wav" />
</audio>

###### Sample 2 
<pre>Benign transcription:       <em>加强 合作社 辅导 员 队伍 建设</em>
Adversarial transcription:  <em>发行 利率 也有 较大 幅度 上升</em>
</pre> &nbsp;
[**benign**: *CER*=8.33],               [**noisy**: *CER*=25.00, SNR<sub>seg</sub>=1.05]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0904W0207_benign.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0904W0207_noisy.wav" type="audio/wav" />
</audio>
[**C&W adversarial**: *CER*=0.00, SNR<sub>seg</sub>=22.48],   [**psychoacoustic**: *CER*=0.00, SNR<sub>seg</sub>=25.82]
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0904W0207_cw.wav" type="audio/wav" />
</audio>
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0904W0207_psy.wav" type="audio/wav" />
</audio>
[**adaptive adversarial**: *CER*=0.00, SNR<sub>seg</sub>=-2.87]
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Aishell/BAC009S0904W0207_gc.wav" type="audio/wav" />
</audio>
