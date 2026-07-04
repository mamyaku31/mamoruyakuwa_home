<script src="https://unpkg.com/jspsych@7.3.2"></script>

<script src="https://unpkg.com/@jspsych/plugin-html-keyboard-response@1.1.2"></script>
<script src="https://unpkg.com/@jspsych/plugin-html-button-response@1.1.2"></script>
<script src="https://unpkg.com/@jspsych/plugin-survey-text@1.1.2"></script>
<script src="https://unpkg.com/@jspsych/plugin-browser-check@1.0.0"></script>
<script src="https://unpkg.com/@jspsych/plugin-preload@1.1.2"></script>

<script src="https://unpkg.com/@jspsych/plugin-survey-multi-choice@1.1.2"></script>

<script src="https://unpkg.com/@jspsych-contrib/plugin-pipe"></script>


<link href="https://unpkg.com/jspsych@7.3.2/css/jspsych.css" rel="stylesheet"/>

# Materials

## このページについて

このページでは八鍬が作成した研究に使えるリソースを公開します。

ここで紹介するものは実験の作成に活用できるjsPsychや、統計分析のためのR、Pythonなどのプログラミングに関する情報が主となります。

QiitaやZennのようなコミュニティに投稿した記事を少しづつ上げていきます。査読を経たものではありませんので間違いやご指摘がございましたらご連絡いただけると幸いです。

## 統計・R

### [Rで始める最大エントロピー調和文法](https://qiita.com/mamyaku31/items/cd4a324f9e5f7c6cd4a0)

Rを使って最大エントロピー調和文法における制約の重みと候補の確率を計算する方法を紹介します。プログラムはそれほど難しくないのでRの基本が理解できている人であればすぐにできると思います。

## オンライン実験 (jsPsych, lab.js, JavaScript, TypeScirpt 等)

<script>
  const jsPsych = initJsPsych({
  show_progress_bar: true,
  message_progress_bar: "終了まで",
  auto_update_progress_bar: true,
  on_finish: function() {
    window.location = "https://google.com"
  }
});

  const welcome = {
    type: jsPsychHtmlButtonResponse,
    prompt: "<p>実験に参加してくださりありがとうございます。</p>",
    stimulus: "",
    choices: "次へ進む",
  };

  const bye = {
    type: jsPsychHtmlButtonResponse,
    prompt: "<p>実験に参加いただきありがとうございました。</p>",
    stimulus: "",
    choices: "実験を終了する",
  };

  const timeline = [
    welcome,
    bye,
    ];

  jsPsych.run(timeline);
</script>




  


