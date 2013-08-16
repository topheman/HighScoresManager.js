HighScoresManager.js
====================

Manages high scores, uses localStorage if enabled, fallback to memory if not.

Creating the instance, you can specify how many highscores you want to manage in your top + in options, the key in the localStorage

```js
var _highScoresManager = new HighScoresManager(10,{localStorageKeyName:'mySpecialKey'});
var performance = {
	"score" : 12000
	"level" : 2
}
_highScoresManager.addHighScore(performance.score,performance.level);//adds/sorts the scores - removes the trailing ones and saves them to localStorage
console.log(_highScoresManager.getHighScores());
```

Used in :

* https://github.com/topheman/squares
* https://github.com/topheman/bombs