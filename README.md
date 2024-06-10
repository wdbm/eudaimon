# eudaimon

## setup

```Bash
pip3 install                                 \
    numpy                                    \
    openai                                   \
    pillow                                   \
    pyaudio                                  \
    pyautogui                                \
    SpeechRecognition                        \
    torch                                    \
    git+https://github.com/openai/whisper.git
```

## eudaimon

The script `eudaimon` is a simple interface to an OpenAI model via the OpenAI API. Simply run the script `eudaimon` and any arguments following the script name are taken as text input for the model used. For this script is assumed that the environment variable `OPENAI_API_KEY` is set appropriately.

![](vegetables.png)

## eudaimon_transcribe

The script `eudaimon_transcribe` uses an offline Whisper model to transcribe spoken words live (and an OpenAI key is not needed). Check the script options with `eudaimon_transcribe --help`. It is assumed that the environment variable `DEFAULT_MIC` is set appropriately. Using `eudaimon_transcribe --list_microphones` may assist with setting this variable. On the first use of a selected Whisper model, it may be that the system downloads the model before transcription is possible. Press `Ctrl` + `C` to exit.

In order to avoid excessive terminal output related to system audio, it may be appropriate to run the script with shell redirection like the following:

```Bash
eudaimon_transcribe 2>/dev/null
```

![](Fidel.gif)

## eudaimon_image

```Bash
./eudaimon_image --image=image.png --prompt="What's in this image?"
This image depicts a painting of a cat looking out of a window at a space scene. Outside the window, there is a view of a large planet that resembles Jupiter with its characteristic stripes, as well as a moon. There are also several large spaceships visible in space. In the foreground, next to the cat, there is a table with a glass of red liquid and a plate with some items on it, possibly food or snacks.
```
