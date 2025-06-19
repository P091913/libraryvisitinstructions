# libraryvisitinstructions
### Because this isn't just me running this.. I used AI to do the markdown for me, I had to correct a lot of the instructions as it convereted my instructions. I originally did everything in Word out of habit.

## Monday – Grades K–2

### ColorChanger

**What to Find:**

```js
const colors = ["pink", "skyblue", "lime", "orange", "purple"];
```

**What to Change**
```js
const colors = ["red", "green", "blue", "yellow", "gold"];
```

### DotDrawer
What to Do:

Tap the screen to make blue dots appear.

Change this line:

```js
backgroundColor: "blue"
```
To:
```
backgroundColor: "green"
```


### EmojiPicker
What to Find:

```js
const emojis = ["🐶", "🐱", "🦄", "🐸", "🐙", "🐢"];
```

What to Change:

Add favorite emoji:

```
  const emojis = ["🦕", "🐧", "🐻"];
```


### StorySpinner
What to Do:

Press button to create a story

Modify the story in the code!



### Soundboard
What to Do:
  Tap to hear a sound!
  
What to Change:
```js
<Button title="🐸 Ribbit" />
```
Change to:
```js
<Button title="🐶 Bark" />
```

Go to soundcloud and find a sound to match your new button title!





## Wednesday – Grades 3–6

### ColorChanger
Add a Random Color Button:

```js
<Button title="Random Color" onPress={() => {
  const index = Math.floor(Math.random() * colors.length);
  setBgColor(colors[index]);
}} />
```

### DotDrawer
Make Dots Bigger:

Find
```js 
width: 20, height: 20
```
Change to:

```js
width: 40, height: 40
```

### EmojiPicker
Add “Clear” Button:

```js 
<Button title="Clear" onPress={() => setEmoji("")} />
```

### StorySpinner
Add New Story:

"A sea turtle became a DJ that flew to the moon..?!"


Soundboard
Add a New Button:

```js
<Button title="Boom!" onPress={() => playSound("https://www.soundjay.com/button/beep-01.wav")} />
```


### Thursday – Grades 7–12

## ColorChanger
Add Reset Button:

```js
<Button title="Reset" onPress={() => setBgColor("white")} />
```

## DotDrawer
Track Dot Count:

```js
const [count, setCount] = useState(0);

setDots([...dots, { x: locationX, y: locationY }]);
setCount(count + 1);
```

Display Count:
```html
<Text style={{ padding: 10 }}>{count} dots placed</Text>
```

## EmojiPicker
Track Emoji History:

```js
const [history, setHistory] = useState([]);

onPress={() => {
  setEmoji(e);
  setHistory([...history, e]);
}}
```
Display History:
```js
<Text>{history.join(" ")}</Text>
```

## StorySpinner
Track Story Log:

```
const [log, setLog] = useState([]);

onPress={() => {
  const random = Math.floor(Math.random() * stories.length);
  const chosen = stories[random];
  setStory(chosen);
  setLog([...log, chosen]);
}}
```
Display Log:
```js
log.map((s, i) => <Text key={i}>{s}</Text>)
```

## Soundboard
Dynamic Sound Array:
```js
const sounds = [
  { label: "Ribbit", url: "https://www.soundjay.com/button/beep-07.wav" },
  { label: "Zoom", url: "https://www.soundjay.com/button/beep-10.wav" },
  { label: "Boom", url: "https://www.soundjay.com/button/beep-01.wav" },
];

{sounds.map((sound) => (
  <Button key={sound.label} title={sound.label} onPress={() => playSound(sound.url)} />
))}
```
