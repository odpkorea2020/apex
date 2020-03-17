# Module 1: REST 엔드포인트 만들기 - 예제 테이블 생성과 REST 활성화

'**모듈 1**'에서는 샘플 데이터셋을 만들어  임포트하고 REST 엔드포인트를 만들어 볼 것입니다. 그리고 REST 엔드포인트를 살펴볼 것입니다. 이 URL은 웹 소스 모듈에서 사용됩니다.

### **Part 1**: 첫 번째 워크스페이스에 EMP와 DEPT 테이블 생성

1. 첫 번째 워크스페이스에 로그인합니다.

2. 메인 메뉴에서 '**SQL Workshop**'을 선택한  후 다시 '**Utilities**'를 선택합니다. 그리고 나서 '**Sample Datasets**'을 클릭합니다.

    ![](images/1/sample-datasets.png)

3. EMP / DEPT 행에서 '**Install**' 버튼을 클릭합니다. 

    ![](images/1/install-emp-dept.png)

4. 그리고 '**Next**' 버튼을 클릭합니다. 그리고 다음 페이지에서 '**Install Dataset**'을 클릭합니다. 그리고 마지막 페이지에서 '**Exit**' 버튼을 클릭합니다.  

** 테이블에서 직접 애플리케이션을 생성하는 것을 원치 않습니다.** 

### **Part 2**: 테이블에 REST 활성화

1. 메인 메뉴에서 '**SQL Workshop**'을 선택한 후, '**SQL Scripts**'를 클릭합니다.

    ![](images/1/select-sql-script.png)

2. '**Create**' 버튼을 클릭합니다. 

    ![](images/1/click-create.png)

3. 다음 URL을 브라우저의 새로운 창에서 실행합니다. 

http://www.oracle.com/technetwork/developer-tools/apex/application-express/apex-hol-rest-enable-5478504.txt

4. 스크립트 편집기에서 - 
    - 'Script Name' 항목에 "**Manual REST on EMP and DEPT**"을 설정합니다.
    - 스크립트 편집기에 위 파일의 내용을 복사해 넣습니다. 
    - '**Run**' 버튼을 클릭합니다.

    ![](images/1/script-name.png)

    - '**Run Now**'를 클릭합니다.
    **4개 Statement가 처리 성공되었다는 결과가 출력됩니다.**

    ![](images/1/scripts-created.png)

### **Part 3**: Reviewing the REST Services

1. 메인 메뉴에서 '**SQL Workshop**'을 선택한 후, '**RESTful Services**'를 클릭합니다.

2. 왼편 트리에서 '**Modules**'를 클릭하여 확대합니다. 계속해서 '**emp.rest**'를 선택하고 확대한 후 '**hol/**' 선택하고 확대합니다. 그리고 '**GET**'을 클릭합니다.

    ![](images/1/copy-url.png)

3. 전체 URL을 클립보드에 복사합니다.

4. 브라우저의 새로운 탭이나 윈도를 만들고 앞에서 복사한 URL을 복사해 넣고 실행합니다. 

    ![](images/1/open-url.png)

## 정보

'Part 2'에서 실행한 SQL 스크립트는 스키마에 REST를 활성화하고 EMP 및 DEPT 테이블 및 EMP_DEPT_V 뷰를 위한 모듈과 핸들러를  생성합니다.

또한 SQL Workshop > RESTful Services 로 이동한 후 스키마에 REST를 직접 활성화할 수 있습니다. 메인 메뉴에서 SQL Workshop > Object Browser로 가서 각 테이블/뷰를 클릭한 다음 REST 탭을 선택하고 REST 서비스를 정의합니다. 그러나 핸들러는 호출될 때마다 데이터 딕셔너리 조회를 이용할 것입니다. 이 방식은 'Part 2'의 방식과 비교할 때 비효율적입니다. apex.oracle.com과 같은 서비스는 20,000개 이상의 스키마와 엄청나게 큰 데이터 딕셔너리를 사용합니다. 이런 환경에서 수작업으로 REST를 활성화하는 방식을 사용하기에는 무리가 있습니다. 

## Summary

"Module 1"을 완성했습니다. 예제 데이터로 EMP 및 DEPT 테이블을 생성하고 첫 번째 Workspace에 REST 엔드포인트를  구축했습니다. 다음 Module에서 데이터를 렌더링하는 방법에 대하여  알아 볼 것입니다. [이 링크를 클릭하여 'Module 2'로 넘어가시기 바랍니다.](2-building-your-app-which-will-be-based-on-the-rest-endpoints-creating-the-app.md)