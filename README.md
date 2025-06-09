
---

# 🎶 Lofi MIDI Generator with LSTM Neural Network

This project is a deep learning-based **music generation app** that takes a MIDI file as input, learns its note/chord sequences, and generates new lofi-style piano music. Built with **Keras, and music21**, it demonstrates how sequence modeling using LSTMs can create coherent musical compositions.

## 🧠 How It Works

1. **MIDI Parsing**: Extracts notes and chords from an uploaded MIDI file using `music21`.
2. **Sequence Preparation**: Converts notes into integer sequences to train on musical patterns.
3. **Model Architecture**:

   * 3 stacked LSTM layers (512 units each)
   * Dropout + Batch Normalization for regularization
   * Dense layers to predict the next note
4. **Music Generation**: Picks a random sequence and generates \~200 new notes.
5. **Output**: The generated sequence is saved as a downloadable `.mid` file.

---

## 🚀 Features

* Upload any MIDI file as input
* Generates new piano-based MIDI music
* Streamlit UI for easy web interaction
* Pre-trained model included (`final_weights.hdf5`)
* One-click download for the generated music

---

## 🛠️ Tech Stack

* Python
* [Keras](https://keras.io/) (LSTM-based RNN)
* [music21](https://web.mit.edu/music21/) (for MIDI parsing/composition)
* Pickle (for note serialization)

---

## 🧪 Try It Out

To run locally:

```bash
git clone https://github.com/yourusername/lofi-midi-generator.git
cd lofi-midi-generator
pip install -r requirements.txt
streamlit run app.py
```

Upload a `.mid` file and wait for your custom-generated lofi piece!

---

## 📝 Sample Output

* Example input: a simple piano MIDI piece
* Generated output: [`lofi_output4.mid`](./lofi_output4.mid)

---

## 📁 File Structure

```bash
.
├── final_weights.hdf5        # Pre-trained LSTM model weights
├── app.py                    # Main Streamlit app script
├── lofi_output4.mid          # Sample generated output
├── notes                     # Pickled list of parsed notes
├── requirements.txt          # Required packages
└── README.md                 # This file
```

---

## 📌 Notes

* The model works best on piano MIDI files with clear melodies.
* `notes` file is overwritten on each run.
* Extendable to other instruments or genres with retraining.

---

## 🧠 Future Improvements

* Add melody conditioning (e.g., style transfer from specific genres)
* Fine-tune generation length and structure
* Add real-time MIDI playback in browser
* Dockerize for portable deployment

---

## 🤖 Author

Built by a deep learning enthusiast exploring generative art and AI + music fusion.


---

## 📜 License

MIT License. See `LICENSE` for more details.

---


