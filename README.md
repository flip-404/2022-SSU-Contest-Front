# 프로젝트 설명
`토킹핸드`는 글을 읽지 못하는 청각 장애인을 위한 수어 번역기를 개발하여 접근성을 높이고 교육 환경을 개선하는 것을 목표로 합니다. 음성 인식과 OCR 기능을 추가하여 더욱 향상된 사용자 경험을 제공합니다. 교내 SW공모전에서 학장상을 수상하였으며, 접근성에 대한 지속적인 연구와 개발을 통해 장애인 복지를 개선하고자 합니다.

<div align="center">
<img width="700" alt="image" src="https://github.com/flip-404/2022-SSU-Contest-Front/assets/87515256/fbbd8a20-e7f4-4ab8-b895-516b2df7b61c">
</div>
# 사용 기술 및 라이브러리
Web: ReactJS, react-speech-kit, Tesseract.js, SCSS <br/>
Server: Django, Gunicorn, SQLite<br/>
Cloud: AWS<br/>
공통: Git, Slack, Figma



# 아키텍처

```mermaid

graph TD
    
    
    subgraph "클라이언트 사이드"
        A1[React.js]
        A2[SCSS]
        A3[React Speech Kit]
        A4[Tesseract.js]
    end
    
    subgraph "서버 사이드"
        B1[Django]
        B2[Gunicorn]
    end
    
    subgraph "데이터베이스 및 클라우드"
        C1[SQLite]
        C2[AWS]
    end
    
    subgraph "협업 및 디자인"
        D1[Git]
        D2[Slack]
        D3[Figma]
    end
    
    A1 --> A2
    A1 --> A3
    A1 --> A4
    A1 -->|HTTP 요청| B1
    B1 -->|WSGI 서버| B2
    B1 -->|데이터 처리| C1
    B2 -->|배포| C2
    B1 -->|응답| A1
    
    classDef tools fill:#f9f,stroke:#333,stroke-width:2px;
    D1:::tools
    D2:::tools
    D3:::tools

```
