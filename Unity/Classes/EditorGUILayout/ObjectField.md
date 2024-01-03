
```cs
EditorGUILayout.ObjectField(Object obj, Type objType, bool allowSceneObjects, params GUILayoutOption[] options);

EditorGUILayout.ObjectField(string label, Object obj, Type objType, bool allowSceneObjects, params GUILayoutOption[] options);

EditorGUILayout.ObjectField(GUIContent label, Object obj, Type objType, bool allowSceneObjects, params GUILayoutOption[] options);
```

<table border=1px style="border-collapse:collapse;">
	<tr style="background-color:#333;">
		<th style="padding:5px;"> 파라미터 </th>
		<th style="padding:5px;"> 설명 </th>
	</tr>
	<tr>
		<td style="padding:5px;"> lable </td>
		<td style="padding:5px;"> 필드 앞에 기재하는 레이블 </td>
	</tr>
	<tr>
		<td style="padding:5px;"> obj </td>
		<td style="padding:5px;"> 필드가 표시하는 객체 </td>
	</tr>
	<tr>
		<td style="padding:5px;"> type </td>
		<td style="padding:5px;"> 할당할 수 있는 객체의 형식 </td>
	</tr>
	<tr>
		<td style="padding:5px;"> allowSceneObject </td>
		<td style="padding:5px;"> Scene 오브젝트의 할당 가능 여부<br/>(Hierachy의 오브젝트 사용 여부) </td>
	</tr>
	<tr>
		<td style="padding:5px;"> options </td>
		<td style="padding:5px;"> 추가 레이아웃 속성 </td>
	</tr>
</table>
