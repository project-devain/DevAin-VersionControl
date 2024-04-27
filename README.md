# Devain VersionControl

Devain VersionControl은 Devain 프로젝트에서의 라이브러리 버전 통일을 위해 구성된 템플릿 프로젝트입니다.

코틀린 및 공용 라이브러리의 버전을 해당 프로젝트를 종속성으로 추가하여 사용하면 버전이 통일됩니다.

## 종속성 전이 목록

| 종속성                     | 버전       | 최소 버전 포함 여부 |
|-------------------------|----------|-------------|
| Kotlin                  | 1.8.20   | O           |
| Kotlin Reflection       | 1.8.20   | O           |
| Koin Core               | 3.4.0    | O           |
| ArrowKt Core            | 1.2.4    | O           |
| Kotlinx Coroutines Core | 1.7.3    | O           |
| Sqlite JDBC             | 3.34.1.0 | X           |
| JSON Simple             | 1.1.1    | X           |

## 종속성 추가

build.gradle에 다음과 같이 추가합니다 :

```groovy
repositories {
   maven {
      url "https://repo.trinarywolf.net/releases"
   }
}

depdendencies {
   // minimal은 최소한의 종속성을, full은 모든 종속성을 추가합니다.
   // 둘 중 하나만 선택하여 사용하는것이 권장됩니다.
   
   // 최소한의 종속성을 추가합니다.
   implementation "skywolf46:devain-version-minimal:1.3.0"
   // 모든 종속성을 추가합니다.
   implementation "skywolf46:devain-version-full:1.3.0"
}
```