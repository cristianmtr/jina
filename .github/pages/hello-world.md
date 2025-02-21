# Jina "Hello, World!" 👋🌍

Just starting out? Try Jina's "Hello, World" - `jina hello --help`

## 👗 Fashion Image Search


<a href="https://docs2.jina.ai/">
<img align="right" width="25%" src="https://github.com/jina-ai/jina/blob/master/.github/images/hello-world.gif?raw=true" />
</a>

A simple image neural search demo for [Fashion-MNIST](https://hanxiao.io/2018/09/28/Fashion-MNIST-Year-In-Review/). No extra dependencies needed, simply run:

```bash
jina hello fashion  # more options in --help
```

...or even easier for Docker users, **no install required**:

```bash
docker run -v "$(pwd)/j:/j" jinaai/jina hello fashion --workdir /j && open j/hello-world.html
 replace "open" with "xdg-open" on Linux
```

<details>
<summary>Click here to see console output</summary>

<p align="center">
  <img src="https://github.com/jina-ai/jina/blob/master/.github/images/hello-world-demo.png?raw=true" alt="hello world console output">
</p>


</details>
This downloads the Fashion-MNIST training and test dataset and tells Jina to index 60,000 images from the training set. Then it randomly samples images from the test set as queries and asks Jina to retrieve relevant results. The whole process takes about 1 minute.


## 🤖 Covid-19 Chatbot

<a href="https://docs2.jina.ai/">
<img align="right" width="25%" src="https://github.com/jina-ai/jina/blob/master/.github/images/helloworld-chatbot.gif?raw=true" />
</a>

For NLP engineers, we provide a simple chatbot demo for answering Covid-19 questions. To run that:
```bash
pip install --pre "jina[chatbot]"

jina hello chatbot
```

This downloads [CovidQA dataset](https://www.kaggle.com/xhlulu/covidqa) and tells Jina to index 418 question-answer pairs with DistilBERT. The index process takes about 1 minute on CPU. Then it opens a web page where you can input questions and ask Jina.

<br><br><br><br>

## 🪆 Multimodal Document Search

<a href="https://youtu.be/B_nH8GCmBfc">
<img align="right" width="25%" src="https://github.com/jina-ai/jina/blob/master/.github/images/helloworld-multimodal.gif?raw=true" />
</a>

A multimodal-document contains multiple data types, e.g. a PDF document often contains figures and text. Jina lets you build a multimodal search solution in just minutes. To run our minimum multimodal document search demo:
```bash
pip install --pre "jina[multimodal]"

jina hello multimodal
```

This downloads [people image dataset](https://www.kaggle.com/ahmadahmadzada/images2000) and tells Jina to index 2,000 image-caption pairs with MobileNet and DistilBERT. The index process takes about 3 minute on CPU. Then it opens a web page where you can query multimodal documents. We have prepared [a YouTube tutorial](https://youtu.be/B_nH8GCmBfc) to walk you through this demo.
