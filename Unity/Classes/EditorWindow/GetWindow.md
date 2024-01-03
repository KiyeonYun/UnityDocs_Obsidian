
```cs
EditorWindow.GetWindow(Type t, bool utility, string title, focus);
```

<table border=1px style="border-collapse:collapse;">
	<tr style="background-color:#333;">
		<th style="padding:5px;"> parameter</th>
		<th style="padding:5px;"> default </th>
		<th style="padding:5px;"> 설명 </th>
	</tr>
	<tr>
		<td style="padding:5px;"> t </td>
		<td style="padding:5px;"> - </td>
		<td style="padding:5px;"> EditorWindow를 상속받은 클래스 형식 </td>
	</tr>
	<tr>
		<td style="padding:5px;"> utility </td>
		<td style="padding:5px;"> false </td>
		<td style="padding:5px;"> bool:  </td>
	</tr>
	<tr>
		<td style="padding:5px;"> title </td>
		<td style="padding:5px;"> null </td>
		<td style="padding:5px;"> 창의 제목. null값이면 클래스 이름을 제목으로 사용한다. </td>
	</tr>
	<tr>
		<td style="padding:5px;"> focus </td>
		<td style="padding:5px;"> true </td>
		<td style="padding:5px;"> 창이 이미 존재하는 경우 창에 포커스할지 여부. 새 창 생성시에는 항상 포커스된다. </td>
	</tr>
</table>
