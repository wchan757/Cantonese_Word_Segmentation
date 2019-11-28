# Cantonese Word Segmentation

It is a Cantonese dictionary for Cantonese word segmentation.You can use jieba and load this dictionary as custom dictionary to do the Cantonese word segmentation. 

This Cantonese dictionary is developed through the following sources:
1. https://www.reddit.com/r/Cantonese/comments/62i3ud/most_common_cantonese_words_frequency_list/

2. https://words.hk/faiman/analysis/existingcharpronunciations/DATA


3. http://pycantonese.org/

4. https://fasttext.cc/docs/en/pretrained-vectors.html

## Installation

Download the file wordlist.txt
```
## Usage
import jieba
jieba.load_userdict('wordlist.txt')

Performance: 
1.'影相呃like真係一件好煩嘅事嚟㗎，不過呃like都唔一'
my_dict : [影相, 呃like, 真係, 一件, 好煩, 嘅, 事, 嚟, 不過, 呃like, 都,...]
jieba_dict: [影相, 呃, like, 真, 係, 一件, 好, 煩, 嘅, 事, 嚟, 㗎, ，...]

2.'真係唔好怪人哋叫香港做投訴之都⋯⋯繼有餐廳
my_dict : [真係, 唔好, 怪人, 哋, 叫, 香港, 做, 投訴, 之, 都, 繼, 有, 餐廳, ...]
jieba_dict : [', 真, 係, 唔, 好, 怪人, 哋, 叫, 香港, 做, 投訴, 之, 都, ⋯,]
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
