## Text-to-Speech & Podcast Generator

Formatmaskinen är ett kraftfullt verktyg för text-till-tal och podcast-generering som konverterar text, filer och URL:er till högkvalitativt ljud med hjälp av ElevenLabs AI-röster. Verktyget kan också generera naturliga AI-konversationer och podcasts med LiteLLM-integration.

### Funktioner

- **Text-till-tal konvertering**: Konvertera vanlig text till naturligt tal
- **Filbearbetning**: Extrahera och konvertera text från PDF, DOCX, TXT och Markdown-filer
- **URL-innehållsextraktion**: Extrahera och konvertera webbsidor och online-PDF:er till tal
- **AI Podcast-generering**: Skapa dynamiska konversationspodcasts med flera röster
- **Flerspråksstöd**: Stödjer 16+ språk inklusive svenska, engelska, tyska, franska, etc.
- **Flera röstalternativ**: Välj mellan olika AI-röster med olika accenter och stilar
- **Förbättrade konversationer**: Generera naturliga dialoger med LiteLLM AI-modeller
- **Dra-och-släpp gränssnitt**: Enkel filuppladdning med dra-och-släpp-stöd

### Installation

1. Installera beroenden:
```bash
pip install -r requirements.txt
```

2. Kopiera miljövariabel-exempel och lägg till dina API-nycklar:
```bash
cp .env.example .env
```

3. Redigera `.env` och lägg till dina API-nycklar:
```
ELEVENLABS_API_KEY=din_elevenlabs_api_nyckel
LITELLM_API_KEY=din_litellm_api_nyckel
```

4. Kör applikationen:
```bash
python text_to_speech.py
```

5. Öppna din webbläsare och navigera till:
```
http://localhost:8000
```

### Krav

```
flask
flask-cors
litellm
httpx
pydantic
python-dotenv
PyPDF2
pdfplumber
python-docx
chardet
requests
beautifulsoup4
lxml
```

### Konfiguration

#### Miljövariabler

- `ELEVENLABS_API_KEY`: Din ElevenLabs API-nyckel för text-till-tal
- `LITELLM_API_KEY`: Din LiteLLM API-nyckel för AI-dialoggenerering
- `LITELLM_BASE_URL`: LiteLLM proxy URL (standard: https://anast.ita.chalmers.se:4000)

#### Stödda filformat

- PDF (.pdf)
- Microsoft Word (.docx)
- Textfiler (.txt)
- Markdown (.md)

#### Tillgängliga språk

Svenska (sv), Engelska (en), Tyska (de), Franska (fr), Spanska (es), Italienska (it), Portugisiska (pt), Polska (pl), Turkiska (tr), Ryska (ru), Nederländska (nl), Tjeckiska (cs), Arabiska (ar), Kinesiska (zh), Japanska (ja), Koreanska (ko)

### API Endpoints

#### Text-till-tal
- `POST /api/tts` - Konvertera text till tal
- `POST /api/tts/file` - Konvertera filinnehåll till tal
- `POST /api/tts/url` - Konvertera URL-innehåll till tal

#### Innehållsextraktion
- `POST /api/file/extract` - Extrahera text från uppladdad fil
- `POST /api/url/extract` - Extrahera text från URL

#### Podcast-generering
- `POST /api/podcast/enhanced` - Generera AI-konversationspodcast
- `GET /api/podcast/templates` - Hämta tillgängliga konversationsmallar
- `GET /api/podcast/voices` - Hämta tillgängliga podcast-röster

#### Information
- `GET /health` - Kontrollera API-hälsa och tillgängliga funktioner
- `GET /api/voices` - Lista alla tillgängliga röster
- `GET /api/supported-formats` - Lista stödda filformat

### Röstval

#### Standardröster
- **Charlotte** - Svensk kvinnlig röst
- **Sarah** - Amerikansk kvinnlig röst
- **George** - Brittisk manlig röst
- **Charlie** - Australisk manlig röst
- **Aria** - Amerikansk kvinnlig röst (hes)
- **River** - Neutral amerikansk röst

#### Konversationsmallar
- **Casual Chat** - Vänlig konversation mellan jämlikar
- **Tech Interview** - Professionell teknisk diskussion
- **News Analysis** - Analytisk nyhetsdiskussion
- **Educational** - Undervisningsfokuserat innehåll
- **Storytelling** - Narrativdriven presentation

### Användning

Verktyget kan användas via webbgränssnittet eller direkt via API:et. Webbgränssnittet har fyra huvudflikar:

1. **Text**: Direkt textinmatning för
