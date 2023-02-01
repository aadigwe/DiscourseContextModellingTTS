# Approaches on Contextual Modelling for Conversational TTS

**Abstract:** This repo re-implements the model architecture from recent research studies that have proposed dialogue context modelling methods for predicting context-appropriate prosody for conversational turns within a dialogue.

<table>
  <tr>
    <th>Model</th>
    <th>Features</th>
    <th>Option</th>
    <th>Implemented</th>
    <th>Paper Link</th>
  </tr>
  <tr>
    <td>Guo Context Encoder</td>
    <td>BERT encodings + GRU</td>
    <td>"Guo"</td>
    <td>Done</td>
    <td>[Paper](https://arxiv.org/pdf/2005.10438.pdf)</td>
  </tr>
  <tr>
    <td>Acoustic Context Encoder</td>
    <td>BERT encodings + GRU</td>
    <td>"ACE"</td>
    <td>Done</td>
    <td>[Paper](https://arxiv.org/pdf/2005.10438.pdf)</td>
  </tr>
  <tr>
    <td>Cross-Modal</td>
    <td>GSTs and BERT w/cross-modal attention</td>
    <td>"Cross-Modal"</td>
    <td>In-Progress</td>
    <td>[Paper](https://arxiv.org/pdf/2005.10438.pdf)</td>
  </tr>
    <tr>
    <td>DialogCGN</td>
    <td>BERT + Tacootron Prent, GSTs. DialogCGN </td>
    <td>"DialogCGN"</td>
    <td>In-Progress</td>
    <td>[Paper](https://arxiv.org/pdf/2005.10438.pdf)</td>
  </tr>
</table>

# Dataset

Use DailyTalk data - which can be accessd here You can download our [dataset](https://drive.google.com/drive/folders/1WRt-EprWs-2rmYxoWYT9_13omlhDHcaL).

# Pretrained Models

You can download the pretrained model for the graphical model here[here]().

Toggle the type of contextual method by

```yaml
# In the model.yaml
history_encoder:
  type: "Guo" # ["none", "Guo"]
context_encoder:
  type: "none" # ["none", "Guo", "ACE", "StyleToken", "DialogCGN", "Cross-Modal"]
gst:
  type: "none" # ["gst", "wst"]
```

# Quickstart

## Dependencies

You can install the Python dependencies with

```
pip3 install -r requirements.txt
```

## Inference

See Samples here [ConversationalTTS](https://github.com/keonlee9420/STYLER)

# Training

## Data Preparation

## Training

Train your model with

```
python3 train.py --dataset DailyTalk
```

# Notes

- Updated the Dataloader to other features from the dialogue context

## Model References

- [keonlee9420's STYLER](https://github.com/keonlee9420/STYLER)
- [keonlee9420's Expressive-FastSpeech2](https://github.com/keonlee9420/Expressive-FastSpeech2)
- [keonlee9420's Comprehensive-Transformer-TTS](https://github.com/keonlee9420/Comprehensive-Transformer-TTS)

## FastSpeech2 + Data References

- [keonlee9420's STYLER](https://github.com/keonlee9420/STYLER)
- [keonlee9420's Expressive-FastSpeech2](https://github.com/keonlee9420/Expressive-FastSpeech2)
- [keonlee9420's Comprehensive-Transformer-TTS](https://github.com/keonlee9420/Comprehensive-Transformer-TTS)
