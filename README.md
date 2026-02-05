# AI-assisted-GPA
Built with Java, Spring Boot, Python (ML), and React.js.
 
---

## Currently working on core audio system
- **Audio Source** - This is just an interface which allows you to retrieve audio availability, audio format, and the audio stream. Does not care whether audio is coming from file or live microphone/audio device.
- **File Audio Source** - This will point to a WAV file, verify it exists, decode it, retrieve format metadata, retrieve a readable audio stream
- **Live Audio Source** - This will check if system has a microphone/audio device, check if requested format is supported, check if dataline can be opened from AudioSystem and then open it.
- **Audio Dispatcher** - Takes in readable stream, reads it, splits it into small audio chunks (called buffers)
- **Pitch Detector** - Check if audio source is available, prepare dispatcher, preprocess audio (noise reduction), Calculate frequency (represents the pitch) using an algorithm. We will also make sure to close audio stream and release buffers after this is done.
- **Note Mapper** - Maps the frequency found in the Pitch Detector to a musical note representation.

---

## Future plans
- **Profiles**
- **Leaderboards**
- **Autosave recordings from session** - Option to toggle autosaving functionality, Ability to display recordings on profile (keep private or show publicly). This would allow users to look back at previous recordings and analyze progress
- **Livestreams**

---
