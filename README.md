# ward-Teatchar
!python -m textblob.download_corpora
from textblob import Word
print("👋 Hello! I'm the Word Teacher.")
print("Type ONE word, and I will analyze it with NLP!")

while True:
  user_word=input("\n Enter a word (or 'quit' to stop)").lower()
  if user_word=="quit":
    print("Goodbye! 👋")
    break

  word=Word(user_word)
  corrected=word.spellcheck()[0][0]

  lemma= Word(corrected).lemmatize('v')

  print(f"\n🔎 NLP Analysis for '{user_word}':")
  print(f"✅ Corrected spelling: {corrected}")
  print(f"🌱 Lemma (base form): {lemma}")
