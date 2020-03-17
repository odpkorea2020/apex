# Module 3: 첫 번째 워크스페이스에서 정의한 REST 서비스 연결: EMP 웹 소스 연결

'Module 3'에서는 첫 번째 워크스페이스에서 정의한 REST Endpoint를 연결하고 'Module 2'에서 생성한 애플리케이션을 위한 Web Source를 만들 것이다. 

### **Part 1**: EMP를 위한 Web Source 추가

1. '**Shared Components**'를 클릭합니다. 

    ![](images/3/click-shared-components.png)

2. '**Data Sources**' 아래에 '**Web Source Modules**'을 클릭합니다.  
    ![](images/3/web-source-modules.png)

3. '**Create**' 버튼을 클릭합니다.
    *기본값: From Scratch.*

5. 'Web Source Type'으로 '**ORACLE REST Data Services**'를 선택합니다.

6. 'Name' 항목으로 '**REST EMP Source**'를 설정합니다.

7. 'URL Endpoint' 항목으로 앞에서 테스트했던 REST URI를 설정합니다. 그리고 '**Next**' 버튼을 클릭합니다.

    - URL은 다음과 유사한 형태를 보입니다.
        - https://<< your service >>/dpeake_rest/emp/hol

    ![](images/3/web-source-type.png)

8. 'Base URL'과 'Service URL 경로를 확인합니다.

9. '**Next**' 버튼을 클릭합니다.

10. '**Discover**' 버튼을 클릭합니다.
    **Authentication Required = No**

11. '**Create Web Source**' 버튼을 클릭합니다.

    ![](images/3/create-web-source.png)

### **Part 2**: 오퍼레이션 추가

1. 'Module Name'에 위치하는 **REST EMP Source** 링크를 클릭합니다.

    ![](images/3/click-rest-emp-source.png)

2. 현재 GET과 POST가 추가되어 있습니다. 

    ![](images/3/click-add-operation.png)

3. '**Add Operation**' 버튼을 클릭하고 다음 설정값을 입력합니다.

    | 속성 | 설정 or 선택 | 설정값 |
    | --- | --- | --- |
    | URL Pattern | 입력 | **:empno** |
    | HTTP Method | 선택 | **GET** |
    | Database Operation | 선택 | **Fetech single row** |
    
    - '**Create**' 버튼을 클릭합니다. 

    ![](images/3/select-database-operation.png)

4.  '**Add Operation**' 버튼을 클릭하고 다음 설정값을 입력합니다.

    | 속성 | 설정 or 선택 | 설정값 |
    | --- | --- | --- |
    | URL Pattern | 입력 | **:empno** |
    | HTTP Method | 선택 | **PUT** |
    | Database Operation | 선택 | **Update row** |
    
    - '**Create**' 버튼을 클릭합니다. 

5. '**Add Operation**' 버튼을 클릭하고 다음 설정값을 입력합니다.

    | 속성 | 설정 or 선택 | 설정값 |
    | --- | --- | --- |
    | URL Pattern | 입력 | **:empno** |
    | HTTP Method | 선택 | **DELETE** |
    | Database Operation | 선택 | **Delete row** |

    - '**Create**' 버튼을 클릭합니다.
    
    ![](images/3/operations.png)
    **3개 오퍼레이션을 만들면 위 이미지와 같이 보입니다.**

6. '**Apply Changes**' 버튼을 클릭합니다.

## 요약

"Module 3"을 완성했습니다. 'Module 1'에서 정의한 REST Endpoint를 연결하는 웹 소스 모듈을 만드는 방법을 실습하였습니다. [이 링크를 클릭하여 'Module 4'로 넘어가시기 바랍니다.](4-defining-the-report-and-form-on-emp-creating-pages.md)
