# Android Coding Convention

출처 : https://github.com/4z7l/Github-WIKI




## 목차

- [1. 기본](#1---)
   * [1.1. 안드로이드 스튜디오](#11-안드로이드-스튜디오)
- [2. Resource Naming Convention](#2-resource-naming-convention)
   * [2.1. ID](#21-id)
      + [2.1.1. Prefix](#211-prefix)
      + [2.1.2. 예시](#212-예시)
   * [2.2. Layout](#22-layout)
      + [2.2.1. Prefix](#221-prefix)
      + [2.2.2. 예시](#222-예시)
   * [2.3. Drawable](#23-drawable)
      + [2.3.1. Prefix](#231-prefix)
      + [2.3.2. 예시](#232-예시)
   * [2.4. Menu](#24-menu)
      + [2.4.1. Prefix](#241-prefix)
   * [2.5. Color](#25-color)
      + [2.5.1. 예시](#251-예시)
   * [2.6. String](#26-string)
      + [2.6.1. Prefix](#261-prefix)
      + [2.6.2. 예시](#262-예시)
   * [2.7. Style](#27-style)
      + [2.7.1. Prefix](#271-prefix)
      + [2.7.2. 예시](#272-예시)



<br>

## 1. 기본

기본적으로 공식문서인 [Kotlin Coding Conventions](https://kotlinlang.org/docs/reference/coding-conventions.html)과 [Kotlin style guide](https://developer.android.com/kotlin/style-guide)를 준수한다.

### 1.1. 안드로이드 스튜디오

안드로이드 스튜디오의 `Optimize imports` 기능과 `Reformat Code` 기능을 이용한다.

- `Optimize imports` `(Ctrl+Alt+O)` : 사용하지 않는 Class를 import하고 있는 경우 제거해준다.
- `Reformat Code` `(Ctrl+Alt+L)` : 코드의 Kotlin Style Guide를 적용하여 Code를 Reformat한다.

<br>

## 2. Resource Naming Convention

### 2.1. ID

View 이름의 Pascal Case를 축약하여 Snake Case로 변환한 것을 Prefix로 사용한다.

#### 2.1.1. Prefix

`<WHAT>_<DESCRIPTION>`

| View                 | Prefix |
| -------------------- | ------ |
| TextView             | `tv_`  |
| ImageView            | `iv_`  |
| EditText             | `et`   |
| Button, ImageButton  | `btn_` |
| Toolbar              | `tb_`  |
| ConstraintLayout     | `cl_`  |
| LinearLayout         | `ll_`  |
| BottomNavigationView | `bnv_` |
| ..                   | ..     |

#### 2.1.2. 예시

```xml
@+id/tv_login
@+id/et_password
@+id/btn_login
```

<br>

### 2.2. Layout

Layout의 xml 파일의 이름은 .kt .java의 Pascal Case를 Snake Case로 변환하여 사용한다.

#### 2.2.1. Prefix

`<WHAT>_<WHERE>`

| View       | Prefix      |
| ---------- | ----------- |
| Activity   | `activity_` |
| Fragment   | `fragment_` |
| Dialog     | `dialog_`   |
| CustomView | `view_`     |
| Item       | `item_`     |

#### 2.2.2. 예시

```
SignInActivity.kt -> activity_sign_in.xml
SignUpFragment.kt -> fragment_sign_up.xml
CustomCalendarView.kt -> view_custom_calendar.xml
item_user.xml
```

<br>

### 2.3. Drawable

#### 2.3.1. Prefix

`<WHAT_DESCRIPTION>`

| Drawable   | Prefix                             |
| ---------- | ---------------------------------- |
| Icon       | `ic_`                              |
| Image      | `img_`                             |
| Background | `bg_`                              |
| Shape      | `<shape>_<color>_<radius>_<value>` |



#### 2.3.2. 예시

```
ic_error.xml
img_default_user.xml
bg_main.xml
rectangle_yellow_radius_20.xml
```



<br>

### 2.4. Menu

#### 2.4.1. Prefix

`menu_`

<br>

### 2.5. Color

Color의 이름은 Camel Case를 이용해 작성하되, [사이트](https://chir.ag/projects/name-that-color/#6195ED)를 참고해 Color를 직관적으로 연상할 수 있는 이름을 사용한다.

#### 2.5.1. 예시

```xml
<color name="black">#FF000000</color>
<color name="white">#FFFFFFFF</color>
<color name="cornflowerBlue">#6195ED</color>
```

<br>

### 2.6. String

String 작성 시 주석을 통해 String이 사용되는 곳을 명시한다.



#### 2.6.1. Prefix

`<WHERE/WHAT>_<DESCRIPTION>` 

#### 2.6.2. 예시

```xml
<!--Main Menu-->
<string name="menu_daily">하루의 기록</string>
<string name="menu_remind">평가 및 회고</string>
<string name="menu_my">My</string>

<!--Toolbar Title-->
<string name="title_search">검색</string>
<string name="title_settings">환경설정</string>

<!--Dialog Message-->
<string name="msg_login">로그인하시겠습니까?</string>
<string name="msg_login_failed">로그인에 실패했습니다.</string>
<string name="msg_password_error">비밀번호가 올바르지 않습니다.</string>
```

<br>



### 2.7. Style

View의 Pascal Case와 Style에 대한 설명을 조합하여 Style 명을 지정한다.

#### 2.7.1. Prefix

`<WHAT><Description>Style`

#### 2.7.2. 예시

```xml
<style name="LoginEditTextStyle"/>
<style name="MainDialogStyle"/>
```




<br><br>

```
Copyright 2020. Seulgi Kim All rights reserved.
```