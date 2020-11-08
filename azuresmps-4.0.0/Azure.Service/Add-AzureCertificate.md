---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046395"
---
# Add-AzureCertificate

## SYNOPSIS
Azure 클라우드 서비스에 인증서를 업로드 합니다.

## 구문과

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**추가-AzureCertificate** Cmdlet은 Azure 서비스에 대 한 인증서를 업로드 합니다.

## 예제의

### 예제 1: 인증서 및 암호 업로드
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

이 명령은 ContosoCertificate 인증서 파일을 클라우드 서비스에 업로드 합니다.
명령은 인증서의 암호를 지정 합니다.

### 예제 2: 인증서 파일 업로드
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

이 명령은 인증서 파일 ContosoCertificate을 클라우드 서비스에 업로드 합니다.
명령은 인증서의 암호를 지정 합니다.

### 예제 3: 인증서 개체 업로드
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

첫 번째 명령은 Windows PowerShell core **Get 항목** cmdlet을 사용 하 여 사용자의 MY store에서 인증서를 가져옵니다.
명령이 $Certificate 변수에 인증서를 저장 합니다.

두 번째 명령은 $certificate의 인증서를 클라우드 서비스에 업로드 합니다.

## 변수

### -CertToDeploy
배포할 인증서를 지정 합니다.
* .Cer 또는 * 파일이 있는 파일과 같은 인증서 파일의 전체 경로를 지정할 수 있습니다.
pfx 파일 이름 확장명 또는 X. x.509 Certificate 개체.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -암호
인증서 암호를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
이 cmdlet이 인증서를 추가 하는 Azure 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### ManagementOperationContext

## 상속자

## 관련 링크

[Get-AzureCertificate](./Get-AzureCertificate.md)

[새로운 AzureCertificateSetting](./New-AzureCertificateSetting.md)

[제거-AzureCertificate](./Remove-AzureCertificate.md)


