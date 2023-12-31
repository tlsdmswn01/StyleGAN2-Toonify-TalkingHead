# MyTalkCon-with-StlyeGAN-Toonify-TalkingHead
 <h2>프로젝트 개요</h2>
        <table class="summary">
            <tr>
              <th>기간</th>
              <td>2023.12.00 ~ 2023.00.00 (약 ~주)</td>
            </tr>
            <tr>
              <th>인원구성</th>
              <td><a href="https://github.com/Leo-Moooon">고예진</a> 
                  <a href="https://github.com/okteam13">신은주</a> 
                  <a href="https://github.com/xxonyuk">이선주</a>
                  <a href="https://github.com/xxonyuk">이정호</a></td>
            </tr>
            <tr>
              <th>프로젝트 목표</th>
              <td>수어 인식이 가능한 챗봇 서비스의 개발을 통한 청각장애인의 의료격차 해소</td>
            </tr>
            <tr>
              <th>프로젝트 내용</th>
              <td>▪ 수어인식 모델 개발 간 GRB 비디오 입력과 keypoint 입력 시의 성능 비교<br>
                  ▪ 챗봇 개발 간 RAG(Retrieval-augmented generation, 검색 증강 생성) 기술의 적용을 통한 답변의 정확성, 신뢰성 향상</td>
            </tr>
            <tr>
              <th>개발환경 <br> (클라우드)</th>
              <td>  <code>CLOUD</code> Google Colab Pro+<br>
                    <code>OS</code>  Linux(Ubuntu 18.04.6 LTS) <br> 
                    <code>CPU</code> Intel Xeon <br> <code>GPU</code> V100 / A100 <br> 
                    <code>RAM</code> 40GB</td>
            </tr>
            <tr>
              <th>사용 언어 및 <br> 기술 스택</th>
              <td>  <code>Language</code>   <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=white"/>
                                            <br> 
                    <code>Editor</code>     <img src="https://img.shields.io/badge/VS Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/Pycharm-000000?style=flat-square&logo=pycharm&logoColor=white"/>
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
                    <code>NLP</code>        <img src="https://img.shields.io/badge/ChatGPT-0f9e7b?style=flat-square&logo=openai&logoColor=white"/>
                                            <img src="https://img.shields.io/badge/LangChain-b3d053?style=flat-square&logo=langchain&logoColor=white"/>
                                            <br> 
                    <code>DB</code>         <img src="https://img.shields.io/badge/ChromaDB-307af8?style=flat-square&logo=chroma&logoColor=white"/>
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
                <li>데이터 수집</li>
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
                <li>추후 개선 방향</li>
            </ol>
        </div>


 
 <div id="service-section">
            <h1>서비스</h1>
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


--- 

# 📃아이디어 제안 배경
- 이모티콘 소비 특징 :
- 개인화 캐릭터 생성 인기 :
  
 ## 페르소나 - 유저 활용기대
 
 ## 유사 서비스와의 차별점
- 유사 서비스 차별점 ppt 이미지 넣기

 <div id="data-section">
            <h1>데이터</h1>
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
                    <td width="300"><img src="./src/images/SSLRV1_full.png" height="300" alt="SSLRV1_full.png"></td>
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
            <br>
            <h3>StyleGAN 한계점</h3>
            <li>부족한 특징 추출로 인한 underfit 현상.</li>
            <li>모델이 학습데이터에 과하게 편향되어 실제 데이터를 제대로 맞추지 못하는 것으로 추정.</li>
            <br>
            <h3 id="stylegan2">StyleGAN2</h3>
            <table class="stylegan2-table">
                <tr>
                    <td width="300"><img src="./src/images/SSLRV2_full.png" height="300" alt="SSLRV2_full.png"></td>                    <td>
                        <ol>
                            <li>모델 선정 이유</li>
                            <ul>
                                <li>많은 데이터를 필요로 하는 Vision Transformer의 특징이 
                                    SSLR V1에서 과소적합(underfit)의 원인이 되었을 것으로 추정</li>
                                <li>신체 키포인트 추출을 통해 특징 추출 극대화</li>
                            </ul>
                            <br>
                            <li>아키텍쳐 특징</li>
                            <ul>
                                <li><strong>특징 추출기 변경</strong>
                                    <ol>
                                        <li>RGB 비디오에서 신체 Keypoint 데이터 추출</li>
                                        <li>별도의 정규화 (Customized Normalization) 진행</li>
                                    </ol>
                                </li>
                                <li>BERT의 구조를 차용하되, 각 block 사이에 Batch Normalization 레이어 추가</li>
                            </ul>
                            <br>
                            <li>참고 자료</li>
                            <ul>
                                <li><em>"Preprocessing for Keypoint-Based Sign Language Translation without Glosses"(Kim & Baek, 2023)</em></li>
                                <li><em>"BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding." Devlin, J., et al. (2019).</em></li>
                            </ul>
                        </ol>
                    </td>
                </tr>
            </table>
            <br>
            <h3 id="strategy01">성능개선 전략 01: FreezeD</h3>
            <p>Mediapipe 라이브러리를 이용한 신체 Keypoint 추출. 그 후 데이터프레임으로 정규화</p>
            <img src="./src/images/SSLRV2_mediapipe.png" alt="">
            <br>
            <h3 id="strategy02">성능개선 전략 02: ADA</h3>
            <p>하단의 레퍼런스에서 제안한 Customized Normalization 기법을 보유 데이터셋에 적합하게 일부 수정하여 코드 구현 및 적용.</p>
            <img src="./src/images/SSLRV2_mediapipe.png" alt="">
            <li>레퍼런스: <em>"Preprocessing for Keypoint-Based Sign Language Translation without Glosses"(Kim & Baek, 2023)</em></li>
            <br>
            <h3 id="strategy03">데이터 정제</h3>
            <p>하단의 레퍼런스에서 제안한 Customized Normalization 기법을 보유 데이터셋에 적합하게 일부 수정하여 코드 구현 및 적용.</p>
            <img src="./src/images/SSLRV2_mediapipe.png" alt="">
            <li>레퍼런스: <em>"Preprocessing for Keypoint-Based Sign Language Translation without Glosses"(Kim & Baek, 2023)</em></li>
            <br>
            <h3 id="strategy-result">성능 개선 후 최종 이미지 생성결과</h3>
            <img src="./src/images/SSLRV2_ablation_study.png" alt="SSLRV2_ablation_study.png">
            <p>Input data를 Keypoint로 변경하고, Customized-Normalization까지 적용하였을 때 가장 높은 성능이 나왔음.</p>
            <br>
            <h2 id="stylegan"> 🖼️ 그림체 입히기 : Toonify</h2>
            <h3 id="stylegan">Toonify 진행과정</h3>
            <img src="./src/images/SSLRV2_ablation_study.png" alt="SSLRV2_ablation_study.png">
            <h3 id="stylegan">2개 Blended Model 비교</h3>
            <h3 id="stylegan">데이터 정제 - Face Alignment</h3>
            <br>
            <h2 id="stylegan"> 🗣️ Talking Head </h2>
            <h3 id="stylegan">SadTalker</h3>
            <h3 id="stylegan">Make It Talk</h3>
            <h3 id="stylegan">데이터 정제 - Semantic Segmentation</h3>
        </div>
        <br>

 </div>
</p>



## 팀원 소개 및 역할 분담  
*알파코 7기 1조* 

|구성원|깃허브 주소|분담 역할|
|:---:|:--:|:--:|
|고예진|[Git](https://github.com/ayun3738)|프로젝트 일정 관리, MIT fine-tuning, 데이터 전처리, <br> Web Ux 구현|
|신은주|[Git](https://github.com/doh0106)|TTS Modeling(Jests-based), 데이터 전처리, Poly-Encoder train, <br> aws 환경 구축, Web Ux 구현|
|이선주|[Git](https://github.com/Kihoon9498)|MIT fine-tuning, 데이터 전처리, whisper pipeline, <br> aws 환경 구축, Web UI, Ux 구현, 웹 서비스 배포|
|이정호|[GIt](https://github.com/suted2)|W2L fine-tuning, Rad-NeRF fine-tuning 데이터 전처리, <br> TOXIC pipeline, TTS 데이터 생성, Web Ux 구현|

</br>  


