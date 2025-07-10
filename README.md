# BlackStone Backend
블랙스톤 백엔드 리포지토리입니다.

---

## 👥 팀원 소개

| 김대현 | 조준용 |
|:---:|:---:
| <img src="" width="180" height="180"> | <img src="" width="180" height="180"> |
| [@]() | [@]() |

---

## ⚙️ Tech Stack

| 기술 | 설명 |
|------|------|
| | |
| | |
| Git | 체계적인 코드 관리 및 협업 |

---

## 🧭 Git Conventions

### 📌 Branch 전략

- 메인 브랜치: `main`
- 기능 개발 시 화면 또는 역할 기준으로 브랜치 명명 (영역/기능 형태)

**작업 흐름**  
1. 기능 이슈 생성 → 번호 발급  
2. `main` → `기능 브랜치` 생성 후 작업  
3. 작업 완료 → `main` 브랜치로 Pull Request 생성

### 📌 작업 템플릿 가이드

작업 유형에 따라 명확하게 커밋 타입을 구분합니다.

| 타입 | 용도 |
|------|------|
| **Feat** | 새로운 기능 추가 |
| **Fix** | 버그 수정 |
| **Refactor** | 코드 리팩토링 (동작 변화 없이 구조 개선) |
| **Docs** | 문서 작성 및 수정 (README, 주석 등) |
| **Style** | 코드 포맷, 네이밍, 세미콜론 등 스타일 변경 (기능 무관) |
| **Test** | 테스트 코드 추가 및 수정 |
| **Chore** | 설정, 빌드, 패키지 등 기타 변경 작업 |

---

/* 회원가입
 * @RestController
public class SignupController {

    @PostMapping("/signup")
    public String signup(@RequestBody SignupRequest request) {
        System.out.println(request.getEmail());
        System.out.println(request.getPassword());
        System.out.println(request.getNickname());
        return "회원가입 완료!";
    }
}

class SignupRequest {
    private String email;
    private String password;
    private String nickname;

    // Getter, Setter 필수
}

// SignupRequest.java
public class SignupRequest {
    private String email;
    private String password;
    private String nickname;

    // 기본 생성자 필수 (JSON 역직렬화 시 필요)
    public SignupRequest() {}

    public String getEmail() { return email; }
    public void setEmail(String email) { this.email = email; }

    public String getPassword() { return password; }
    public void setPassword(String password) { this.password = password; }

    public String getNickname() { return nickname; }
    public void setNickname(String nickname) { this.nickname = nickname; }
}

// SignupController.java
import org.springframework.web.bind.annotation.*;

@RestController
@RequestMapping("/api")
public class SignupController {

    @PostMapping("/signup")
    public String signup(@RequestBody SignupRequest request) {
        // 1. 데이터 받기
        String email = request.getEmail();
        String password = request.getPassword();
        String nickname = request.getNickname();

        // 2. 검증 예시 (단순화된 버전)
        if (email == null || password == null || nickname == null) {
            return "입력값이 부족합니다.";
        }

        // 3. 비밀번호 암호화 (간단한 해시 예시)
        String encryptedPassword = Integer.toHexString(password.hashCode());

        // 4. DB 저장 (여기선 단순 출력만)
        System.out.println("이메일: " + email);
        System.out.println("암호화된 비밀번호: " + encryptedPassword);
        System.out.println("닉네임: " + nickname);

        // 5. 응답
        return "회원가입 성공!";
    }
}

 */

### ✅ Commit 템플릿

```text
타입: 간단한 설명

- 작업한 내용에 대한 구체적인 설명
- 필요한 경우 여러 줄로 상세하게 작성
```

### 📝 Pull Request 템플릿

```txt
타입: 간단한 설명

## 작업 내용
- 무엇을 변경했는지 간단히 작성

## 참고 사항
- 리뷰 시 유의해야 할 사항
```


### 💡 Issue 템플릿

```txt
타입: 이슈 제목

## 이슈 개요
- 어떤 작업인지 간략히 설명해주세요.

## 작업 항목
- [ ] 작업 1
- [ ] 작업 2
- [ ] 작업 3

## 참고 자료
- 관련 문서, 디자인, 링크 등
```

---
