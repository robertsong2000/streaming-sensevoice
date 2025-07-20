# streaming-sensevoice

Streaming SenseVoice processes inference in chunks of [SenseVoice](https://github.com/FunAudioLLM/SenseVoice).

## Usage

- transcribe wav file

```bash
$ python main.py
```

![](images/screenshot.png)

- transcribe from microphone

```bash
$ python realtime.py
```

- transcribe from websocket

A basic WebSocket service built with [`Recorder`](https://github.com/xiangyuecn/Recorder) and `FastAPI`; the frontend uses `MP3` format to transmit audio information to reduce latency and increase stability.

```bash
pip install -r requirements-ws-demo.txt
python realtime_ws_server_demo.py

# check cli options
python realtime_ws_server_demo.py --help
```

### WebSocket Client Features

- Supports automatic language detection (Auto Detect) or specific languages (Chinese, English, Japanese)
- System audio capture support
  - Check the "Capture System Audio" checkbox
  - Select the window or tab to share in the system sharing dialog
  - Make sure to enable "Share system audio" option
  - Adjust appropriate system and microphone volume levels
- Real-time VAD (Voice Activity Detection) status display
- Real-time transcription results with timestamp information
