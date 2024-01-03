
참고자료
- [Unity Docs - 에디터 창](https://docs.unity3d.com/kr/2021.3/Manual/editor-EditorWindows.html)
- [루시라테의 성공일지 블로그](https://rucira-tte.tistory.com/270)

---
## 1. Script 파일 생성

1. Asset 폴더에 <b>Editor</b> 폴더를 생성한 후 그 안에 Script를 생성한다.
![[Pasted image 20231116120444.png]]

2. MonoBehavior 대신 EditorWindow를 상속받는다.
```cs
public class PrefabBrush : EditorWindow
```

---
## 2. Custom Window 띄우기

창을 활성화하는 함수를 선언한다. 
이 때 함수에 어디에서든 접근이 가능해야하기 때문에 static으로 선언한다.
```cs
[MenuItem("Window/Prefab Brush")]
public static void ShowWindow()
{
	EditorWindow.GetWindow(typeof(PrefabBrush));
}
```
MenuItem Property가 EditorWindow.GetWindow를 통해 함수가 활성화된다.

![[Pasted image 20231116120820.png]]

![[Pasted image 20231116121125.png]]

---
## 3. Parameter 생성

```cs
private void OnGui() { }
```
GUI Editor를 구현하는 내장 함수를 통해 parameter를 구현한다.

#### 1) int
```cs
int myInt = EditorGUILayout.IntField("My Int Field", myInt);
```
![[Pasted image 20231116124722.png]]

#### 2) float
```cs
float myFloat = EditorGUILayout.FloatField(myFloat);
```
![[Pasted image 20231116125611.png]]

FloatField에는 label을 붙일 수 없고 가독성이 떨어지기 때문에 아래 Slider를 주로 사용한다.

```cs
float myFloat = EditorGUILayout.Slider("My Slider", myFloat, -3f, 3f);
```
![[Pasted image 20231116125756.png]]![[Pasted image 20231116125807.png]]
창 너비에 따라 슬라이더가 보이지 않을 수도 있다.

#### 3) bool
```cs
bool myBool = EditorGUILayout.Toggle("My Bool Toggle", myBool);
```
![[Pasted image 20231116125004.png]]

#### 4) string
```cs
string myString = EditorGUILayout.TextField("Text Field", myString);
```
![[Pasted image 20231116125204.png]]

#### 5) Label
```cs
GUILayout.Label("My Label 1", EditorStyles.boldLabel);
```

![[Pasted image 20231116130659.png]]
#### 6) Group Toggle

```cs
bool groupEnabled = EditorGUILayout.BeginToggleGroup("My Group Toggle", groupEnabled);
/* Custom parameters */
EditorGUILayout.EndToggleGroup();
```
선언문과 종료문(EndToggleGroup) 사이의 Parameter들을 그룹으로 묶는다.

![[Pasted image 20231116130509.png]]![[Pasted image 20231116130520.png]]
groupEnabled가 false이면 하위 파라미터들을 수정할 수 없다.


#### 7) Object
```cs
Object MyObject = null;
MyObject = EditorGUILayout.ObjectField("My Object Field", MyObject, typeof(GameObject), true);
```
(3번째 인자) GameObject 타입만 넣을 수 있고
(4번째 인자) Hierachy의 오브젝트를 사용할 수 있다. false로 바꾸면 Prefab만 사용 가능하다.
참조: [[ObjectField]]
![[Pasted image 20231116130955.png]]

```cs
Object MyObject = null;
MyObject = EditorGUILayout.ObjectField("My Object Field", MyObject, typeof(Sprite), false);
```
![[Pasted image 20231116150604.png]]


---
## 4. ㅇㅇ
