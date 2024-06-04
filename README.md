# Cantonese Word Segmentation

This repository offers a Cantonese dictionary specifically designed for enhancing Cantonese word segmentation. It allows the integration with the `jieba` segmentation library, enabling you to use it as a custom dictionary for Cantonese text processing.

## Sources

The development of this Cantonese dictionary has been informed by the following resources:

- [Most Common Cantonese Words Frequency List](https://www.reddit.com/r/Cantonese/comments/62i3ud/most_common_cantonese_words_frequency_list/)
- [Words.hk Faiman Analysis](https://words.hk/faiman/analysis/existingcharpronunciations/DATA)
- [PyCantonese](http://pycantonese.org/)
- [FastText Pretrained Vectors](https://fasttext.cc/docs/en/pretrained-vectors.html)

## Installation

To get started, download the dictionary file from the repository:

```bash
Download the file `wordlist.txt`
```

## Usage

You can integrate this dictionary into your `jieba` processing workflow as follows:

```python
import jieba
jieba.load_userdict('wordlist.txt')
```

## Performance Comparison

Here are some examples demonstrating the improvements in segmentation when using this custom dictionary compared to the default `jieba` dictionary:

1. **Example Sentence:**

   `"影相呃like真係一件好煩嘅事嚟㗎，不過呃like都唔一"`

   - **Custom Dictionary Output:**
     `[影相, 呃like, 真係, 一件, 好煩, 嘅, 事, 嚟, 不過, 呃like, 都, ...]`
   - **Jieba Default Dictionary Output:**
     `[影相, 呃, like, 真, 係, 一件, 好, 煩, 嘅, 事, 嚟, 㗎, ...]`

2. **Example Sentence:**

   `"真係唔好怪人哋叫香港做投訴之都⋯⋯繼有餐廳"`

   - **Custom Dictionary Output:**
     `[真係, 唔好, 怪人, 哋, 叫, 香港, 做, 投訴, 之, 都, 繼, 有, 餐廳, ...]`
   - **Jieba Default Dictionary Output:**
     `[真, 係, 唔, 好, 怪人, 哋, 叫, 香港, 做, 投訴, 之, 都, ⋯⋯, ...]`
