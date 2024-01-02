# MyTalkCon-with-StyleGAN-Toonify-TalkingHead
<h2>프로젝트 개요</h2>
        <table class="summary">
            <tr>
              <th>기간</th>
              <td>2023.12.00 ~ 2023.00.00 (약 ~주)</td>
            </tr>
            <tr>
              <th>인원구성</th>
              <td><a href="https://github.com/Leo-Moooon">고예진</a> 
                  <a href="https://github.com/tlsdmswn01">신은주</a> 
                  <a href="https://github.com/xxonyuk">이선주</a>
                  <a href="https://github.com/xxonyuk">이정호</a></td>
            </tr>
            <tr>
              <th>프로젝트 목표</th>
              <td>사용자가 원하는 그림체와 자신 얼굴, 음성을 반영한 소리이모티콘 생성 서비스 제공</td>
            </tr>
            <tr>
              <th>프로젝트 내용</th>
              <td>▪ StyleGAN2, Toonify를 통해 실사 이미지를 이모티콘화<br>
                  ▪ Talking Head를 통한 말하는 나만의 이모티콘 생성</td>
            </tr>
            <tr>
              <th>개발환경 <br> (클라우드)</th>
              <td>  <code>CLOUD</code> Google Colab Pro+<br>
                    <code>OS</code>  Linux(Ubuntu 18.04.6 LTS) <br> 
                    <code>CPU</code> Intel Xeon <br> <code>GPU</code> V100 / A100 <br> 
                    <code>RAM</code> 24GB</td>
            </tr>
            <tr>
              <th>사용 언어 및 <br> 기술 스택</th>
              <td>  <code>Language</code>   <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/>
                                            <br> 
                    <code>Editor</code>     <img src="https://img.shields.io/badge/VS Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white"/>
                                            <br> 
                    <code>Modeling</code>   <img src="https://img.shields.io/badge/Tensorflow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/HuggingFace-f8a700?style=flat-square&logo=huggingface&logoColor=white"/>
                                            <br> 
                    <code>CV</code>         <img src="https://img.shields.io/badge/OpenCV(python)-412991?style=flat-square&logo=opencv&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/Albumentations-d90000?style=flat-square&logo=albumentations&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/TorchVision-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
                                            <br> 
                    <code>Web</code>        <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/AJAX-3087c5?style=flat-square&logo=ajax&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/JQuery-0769AD?style=flat-square&logo=jquery&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white"/>
                                            <br>
                    <code>Logging</code>    <img src="https://img.shields.io/badge/Weights & Biases-FFBE00?style=flat-square&logo=weightsandbiases&logoColor=white"/>
                                            <br> 
                    <code>Version Control</code>        <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
                                            <br>
              </td>
            </tr>
        </table>

 <div id="table-of-contents">
            <h2>목차</h2>
            <ol class="project-ul" start="1">
                <li>서비스</li>
                <ul class="serve-ul">
                    <li><a href="#testing">활용 예시(시연 영상)</a></li>
                    <li><a href="#service-ui">서비스 UI</a></li>
                    <li><a href="#service-architecture">서비스 구조도</a></li>
                </ul>
                <br>
                <li>아이디어 제안배경</li>
                <br>
                <li>데이터</li>
                <ul class="data-ul">
                    <li><a href="#dataselect">데이터 수집</a></li>
                </ul>
                <br>
                <li>아이디어 구현 과정 </li>
                <br>
                <ul class="modeling-ul">
                    <li><a href="#StyleGAN-info">그림체 생성 : StyleGAN2</li>
                       <ul class="StyleGAN-info-ul">
                            <li><a href="#model-pick">모델 선정과정</a></li>
                               <ul class="model-pick-ul">
                                  <li><a href="#stylegan"> StyleGAN</a></li>
                                  <li><a href="#stylegan2"> StyleGAN2</a></li>
                               </ul>
                            <li><a href="#strategy">성능 개선 전략</a></li>
                               <ul class="strategy-ul">
                                  <li><a href="#strategy01"> 01: FreezeD</a></li>
                                  <li><a href="#strategy02"> 02: ADA(데이터 증강 기법)</a></li>
                                  <li><a href="#strategy03"> 03: 데이터 정제</a></li>
                                  <li><a href="strategy-result">성능 개선 후 최종 이미지 생성결과</a></li>
                               </ul>
                       </ul>
                    <br>
                    <li><a href="#Toonify">그림체 입히기 : Toonify</a></li>
                        <ul class="Toonify-ul">
                          <li><a href="#FAQ-section">Toonify 진행과정</a></li>
                          <li><a href="#query-embedding-section">2개 Blended Model 비교</a></li>
                          <li><a href="#return-answer-section">데이터 정제 - FaceAlignment</a></li>
                        </ul>
                   <br>
                   <li><a href="#Talking">Talking Head</a></li>
                        <ul class="Toonify-ul">
                          <li><a href="#FAQ-section">SadTalker</a></li>
                          <li><a href="#query-embedding-section">Make It Talk</a></li>
                          <li><a href="#return-answer-section">데이터 정제 - Semantic Segmentation</a></li>
                        </ul>
                </ul
                <br>
                <br>
                <li>추후 개선 방향</li>
            </ol>
        </div>


 
 <div id="service-section">
            <h1>⭐ 서비스</h1>
            <h2 id="testing">활용 예시</h2>
            <img src="./src/images/service_testing.gif" height="400">
            <br>
            <br>
            <h2 id="service-ui">서비스 UI</h2>
            <img src="./src/images/service_ui.png" height="300" alt="service_ui.png">
            <ul>
                <li>Flask를 이용한 웹서비스 구현</li>
                <li>Socket.IO를 통한 클라이언트-서버 실시간 통신</li>
            </ul>
            <br>
            <br>
            <h2 id="service-architecture">서비스 구조도</h2>
            <img src="./src/images/service_architecture.png" height="500" alt="service_architecture.png">
            <br>
            <br>
        </div>
        <br>

</div>

</p>



# 📃아이디어 제안 배경
- 이모티콘 소비 특징 : 이모티콘 시장이 매우 커짐에 따라 종류가 다양화 되었지만, 여전히 이모티콘 사용자들은 자신이 선호하는 캐릭터 이모티콘을 사용하고 싶은 니즈를 보임
- 개인화 캐릭터 생성 인기 : 2023년 AI 아바타 인기로, 사용자들은 나의 개성이 반영된 개인화 캐릭터 생성에 흥미를 느끼고 관심을 가짐.
  
 ## 페르소나 - 유저 활용기대
 - ppt 만들어지면 넣기
 
 ## 유사 서비스와의 차별점
- 유사 서비스: 미모티콘, 네이버 툰 필터
<br>
  <div align='center'>
  <img width='80%' src="https://github.com/tlsdmswn01/StlyeGAN2-Toonify-TalkingHead/assets/135305102/5234ffc0-303f-4c76-885a-9f59051a626f" width="2000" height="450" />
</div>
 <div id="data-section">
            <h1>💿 데이터</h1>
            <h2 id="data-section">데이터 수집</h2>
            <p>AI Hub - "수어 영상" 데이터셋에서 단어 영상 및 라벨 데이터 취득.</p>
            <ul>
                <li>EDA를 통해 전체 의료 용어 5,485건, 일상어 12,317건을 선별.</li>
                <li>데이터셋에서 제시하는 기준에 맞춰 Train 및 Validation 데이터 구분.</li>
                <li>제공된 Train과 Validation 데이터의 유사성이 높다고 판단하여, Test 데이터는 별도로 촬영하여 소량 수집하였음.</li>
            </ul>
        </div>
        <br>

 <div id="modeling-section">
            <h1>🖥️ 아이디어 구현 과정</h1>
            <br>
            <h2> 🎨 그림체 생성 : StyleGAN2 </h2>
            <h3 id="stylegan">StyleGAN</h3>
            <table class="stylegan-table">
                <tr>
                    <td width="300"><img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/135305102/6d0c9f65-9825-482e-a4fd-24f114993e18"
 height="300" alt="SSLRV1_full.png"></td>
                    <td>
                        <ol>
                            <li>모델 선정 이유</li>
                            <ul>
                                <li>그림체를 입히기 위해, 먼저 스타일 생성 필요</li>
                                <li>기존 GAN을 변형한 형태로, 이미지 생성 시 스타일을 조절할 수 있는 장점을 가짐.</li>
                            </ul>
                            <br>
                            <li>아키텍쳐 특징</li>
                            <ul>
                                <li> Progressive Growing을 통해 고해상도 이미지 생성</li></li>
                                <li>Style Transfer 정규화 방법, AdaIN을 통해 레이어에 이미지와 스타일을 결합</li>
                            </ul>
                            <br>
                            <li>참고 자료</li>
                            <ul>
                                <li><em>"Beyond Short Snippets: Deep Networks for Video Classification"(Ng et al., 2015)</em></li>
                                <li><em>"Attention Is All You Need" (Vaswani, A., et al., 2017)</em></li>
                            </ul>
                        </ol>
                    </td>
                </tr>
            </table>
            <br>
            <h3>StyleGAN 한계점</h3>
            <li>물방울 같은 노이즈 발생 - AdaIN의 정규화로 발생하는 문제</li>
            <li>일부 피쳐들이 얼굴의 움직임을 따르지 않는 문제 - Progressive growing으로 발생하는 문제</li>
             -<br>
         <div align='left'>
                 <img width='49%' src="https://github.com/tlsdmswn01/StlyeGAN2-Toonify-TalkingHead/assets/135305102/8c180285-0901-4016-90c5-b036a23fc6b2" height=250>
                 <img width='50%' src="https://github.com/tlsdmswn01/StlyeGAN2-Toonify-TalkingHead/assets/135305102/c689c88b-a61f-4156-a467-824106766333" height=250>
         </div>
            <br>
            <h3 id="stylegan2">StyleGAN2</h3>
            <table class="stylegan2-table">
                <tr>
                    <td width="400"><img src="https://github.com/tlsdmswn01/StlyeGAN2-Toonify-TalkingHead/assets/135305102/c1a44bda-0045-410d-a84c-443e9352abb8" height="330" alt="SSLRV2_full.png"></td>                    <td>
                        <ol>
                            <li>모델 선정 이유</li>
                            <ul>
                                <li>위 StyleGAN의 개선모델</li>
                                <li>AdaIN 대신 CNN의 가중치 정규화로 물방울 제거</li>
                                <li>Progressive Growing을 제거해 눈과 이의 부자연스러운 문제 개선</li>
                                <li>StyleGAN보다 더 자연스러운 이미지를 생성하며, PPL과 같은 정량적 평가 지표에서 성능이 더 좋음을 확인</li>
                            </ul>
                            <br>
                            <li>아키텍쳐 특징</li>
                            <ul>
                                    <ol>
                                        <li>AdaIN 같은 실제 통계로 정규화 하는 대신, 추정통계로 정규화</li>
                                        <li>Progressive Growing 대신 skip connection을 갖고 있는 계층 생성자를 사용</li>                                        <li>이미지 품질을 위해 PPL을 줄이고 잠재 공간을 매끄럽게 개선</li>
                                    </ol>
                                </li>
                            </ul>
                            <br>
                            <li>참고 자료</li>
                            <ul>
                                <li><em>TERO KARASS, 「ANALYZING AND IMPROVING THE IMAGE QUALITY OF STYLEGAN」, 2020.</em></li>
                            </ul>
                        </ol>
                    </td>
                </tr>
            </table>
            <br>
            <h3 id="strategy01">성능개선 전략 01: FreezeD</h3>
            <p>FreezeD 논문을 통해 GAN 훈련이 오버피팅에 취약하다는 사실을 알게 되었고, 논문에서 제안한 FreezeD를 통해 개선하고자 함</p>
            <p>Discriminator의 전반부 - 특징 추출기를 동렬해 오버피팅을 조절하고 안정적으로 학습 진행</p>
         <div align='center'>
            <img width='80%' src="https://github.com/tlsdmswn01/StlyeGAN2-Toonify-TalkingHead/assets/135305102/c46133df-3b4c-4f0f-a627-51ab4f341003" >
         </div>
            <br>
                     <li>레퍼런스: <em>"SANGWOO MO, 「FREEZE THE DISCRIMINATOR: A SIMPLE BASELINE FOR FINE-TUNING GANS」, 2020, 1P."</em></li>
            <h3 id="strategy02">성능개선 전략 02: ADA (데이터 증강 기법)</h3>
            <p>하단 논문을 통해 이미지 데이터 셋 부족은 Discriminator 오버피팅을 야기해 Generator에게 주는 피드백이 무의미해지면서 결국 Generator도 학습을 제대로 하지 못한다는 사실을 알게 되었다.</p>
        <div align='center'>
            <img width='90%' src="https://github.com/tlsdmswn01/StlyeGAN2-Toonify-TalkingHead/assets/135305102/d9946c63-4953-4602-9da7-74cf25d33003" alt="">
        </div>
         <br>
         - 논문에 따르면 FreezeD+2만 데이터 셋에서 과적합이 일어난 반면, FreezeD+ADA+5천 데이터셋에 대해서는 과적합이 일어나지 않았다. 당시 우리 데이터는 절대적으로 부족했기에 ADA를 필수적으로 적용할 필요성이 있었다.
            <br>   
         <li>레퍼런스: <em>"출처: TERO KERRAS, 「TRAINING GENERATIVE ADVERSARIAL NETWORKS WITH LIMITED DATA」, 2020"</em></li>
            <br>
            <h3 id="strategy03">성능개선 전략 03: 데이터 정제</h3>
            <li>기존 데이터 셋에는 그림체가 통일되어 있지 않거나 채도가 낮은 이미지가 섞여 있었음. 따라서 데이터 정제를 진행함과 동시에 추가적인 데이터를 수집함</em></li>
            <br>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/c43cb7d9-14e3-4dca-9866-48930a5b1572" width="1280" height="520" />
            <br>
            <h3 id="strategy-result">정성평가(그림체, 채도 통일, 데이터 수 증가)</h3>
            <br>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/407a5e62-25cd-4971-a2a3-7f8a725f5bc5" width="1280" height="520" />
            <p>-> 기존 발생했던 문제점들은 없어졌지만 생성된 이미지 가운데 그림체가 깨지는 현상이 발생함. 문제의 원인이 배경에 있다고 판단하여 배경을 제거하고 학습을 진행하였음. </p>
            <h3 id="strategy-result">정성평가(배경 제거)</h3>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/13a23d25-b058-4fea-bf95-4a1ec3f5ede4" width="1280" height="520" />
            <p>기존 문제점들이 개선 된 것을 확인할 수 있음 </p>
            <h2 id="stylegan"> 🖼️ 그림체 입히기 : Toonify</h2>
            <h3 id="stylegan">Toonify 진행과정</h3>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/44cacd06-bbe5-4210-aaec-dcdbe5fa2525" width="1280" height="520" />
            <h3 id="stylegan">2개 Blended Model 비교</h3>
            <div>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/cf6cc014-cf7b-41c9-a48e-a31fdee9e544" height="520" />
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/eb6dbdc5-eea2-4e0f-8813-c38801145014" height="520" />
            </div>
            <h3 id="stylegan">Face Alignment</h3>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/9422eaed-6302-4e0f-8294-25eb5291d56a" width="1280" height="520" />
            <h3 id="stylegan">실제 이미지에 적용</h3>
            <img src="https://github.com/tlsdmswn01/MyTalkCon-with-StlyeGAN-Toonify-TalkingHead/assets/140469725/9624c0b1-b07d-4bac-a865-0db4e8e7e8ba" width="1280" height="520" />
            <br>
            <h2 id="stylegan"> 🗣️ Talking Head </h2>
            <h3 id="stylegan">SadTalker</h3>
            <table class="sadtalker-table">
                <tr>
                    <td width="300"><img src="https://github.com/tlsdmswn01/StyleGAN2-Toonify-TalkingHead/assets/121289391/b22a9188-b0f0-44ba-8d4e-d8a32810a0ae"></td>
                    <td>
                        <ol>
                            <li>모델 선정 이유</li>
                            <ul>
                                <li>수어는 연속된 동작이므로, 행동을 인식하고 분류하는 문제로 파악</li>
                                <li>RGB 비디오를 학습하여 각 동작에 대한 일반화 기대</li>
                            </ul>
                            <br>
                            <li>아키텍쳐 특징</li>
                            <ul>
                                <li>사전학습된 DenseNet-121을 통해 각 프레임 내 특징 추출</li>
                                <li>Transformer-Encoder 구조로, 프레임 간 전후맥락을 고려한 학습 의도</li>
                            </ul>
                            <br>
                            <li>참고 자료</li>
                            <ul>
                                <li><em>"Beyond Short Snippets: Deep Networks for Video Classification"(Ng et al., 2015)</em></li>
                                <li><em>"Attention Is All You Need" (Vaswani, A., et al., 2017)</em></li>
                            </ul>
                        </ol>
                    </td>
                </tr>
            </table>
            <h3 id="stylegan">Make It Talk</h3>  
              <table class="MakeItTalk-table">
                <tr>
                    <td width="300"><img src="https://github.com/tlsdmswn01/StyleGAN2-Toonify-TalkingHead/assets/121289391/91d05dda-ffe5-408f-9195-794d409cf37d" height="300" alt="SSLRV1_full.png"></td>
                    <td>
                        <ol>
                            <li>모델 선정 이유</li>
                            <ul>
                                <li>수어는 연속된 동작이므로, 행동을 인식하고 분류하는 문제로 파악</li>
                                <li>RGB 비디오를 학습하여 각 동작에 대한 일반화 기대</li>
                            </ul>
                            <br>
                            <li>아키텍쳐 특징</li>
                            <ul>
                                <li>사전학습된 DenseNet-121을 통해 각 프레임 내 특징 추출</li>
                                <li>Transformer-Encoder 구조로, 프레임 간 전후맥락을 고려한 학습 의도</li>
                            </ul>
                            <br>
                            <li>참고 자료</li>
                            <ul>
                                <li><em>"Beyond Short Snippets: Deep Networks for Video Classification"(Ng et al., 2015)</em></li>
                                <li><em>"Attention Is All You Need" (Vaswani, A., et al., 2017)</em></li>
                            </ul>
                        </ol>
                    </td>
                </tr>
            </table>
            <h3 id="stylegan">데이터 정제 - Semantic Segmentation</h3>
        </div>
        <br>

 </div>
</p>


## 🕋팀 정보 (Team Information)

안녕하십니까, 저희는 영앤리츠팀입니다. 

<table>
 <tr>
  <td></td>
  <td>Name</td>
  <td>Role</td>
  <td>github</td>
  <td>e-mail</td>
 </tr>

 <tr>
  <td align='center'><img src="https://avatars.githubusercontent.com/u/135305102?v=4" width="50" height="50"></td>
  <td align='center'>고예진</td>
  <td align='center'>Modeling / Dashboard</td>
  <td align='center'><a href="https://github.com/tlsdmswn01"><img src="http://img.shields.io/badge/tlsdmswn01-green?style=social&logo=github"/></a></td>
  <td align='center'><a href="mailto:sinssinej7@ajou.ac.kr"><img src="https://img.shields.io/badge/sinssinej7@ajou.ac.kr-green?logo=gmail&style=social"/></a></td>
 </tr>
 
 <tr>
  <td align='center'><img src="https://avatars.githubusercontent.com/u/135305102?v=4" width="50" height="50"></td>
  <td align='center'>신은주</td>
  <td align='center'>Modeling / Dashboard</td>
  <td align='center'><a href="https://github.com/tlsdmswn01"><img src="http://img.shields.io/badge/tlsdmswn01-green?style=social&logo=github"/></a></td>
  <td align='center'><a href="mailto:sinssinej7@ajou.ac.kr"><img src="https://img.shields.io/badge/sinssinej7@ajou.ac.kr-green?logo=gmail&style=social"/></a></td>
 </tr>
 
 <tr>
  <td align='center'><img src="https://avatars.githubusercontent.com/u/135305102?v=4" width="50" height="50"></td>
  <td align='center'>이선주</td>
  <td align='center'>Modeling / Dashboard</td>
  <td align='center'><a href="https://github.com/tlsdmswn01"><img src="http://img.shields.io/badge/tlsdmswn01-green?style=social&logo=github"/></a></td>
  <td align='center'><a href="mailto:sinssinej7@ajou.ac.kr"><img src="https://img.shields.io/badge/sinssinej7@ajou.ac.kr-green?logo=gmail&style=social"/></a></td>
 </tr>

 <tr>
  <td align='center'><img src="https://avatars.githubusercontent.com/u/135305102?v=4" width="50" height="50"></td>
  <td align='center'>이정호</td>
  <td align='center'>아이디어 기획, StyleGAN2+Fine-tuning, Toonify</td>
  <td align='center'><a href="https://github.com/tlsdmswn01"><img src="http://img.shields.io/badge/tlsdmswn01-green?style=social&logo=github"/></a></td>
  <td align='center'><a href="mailto:sinssinej7@ajou.ac.kr"><img src="https://img.shields.io/badge/sinssinej7@ajou.ac.kr-green?logo=gmail&style=social"/></a></td>
 </tr>
</table>
</br>  


