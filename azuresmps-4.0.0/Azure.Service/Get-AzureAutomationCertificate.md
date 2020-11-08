---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045663"
---
# Get-AzureAutomationCertificate

## SYNOPSIS

Azure Automation 인증서를 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByCertificateName
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationCertificate** cmdlet은 하나 이상의 Microsoft Azure Automation 인증서를 가져옵니다.
기본적으로 모든 인증서가 반환 됩니다.
특정 인증서를 가져오려면 해당 이름을 지정 합니다.

## 예제의

### 예제 1: 모든 인증서 가져오기
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 인증서를 가져옵니다.

### 예제 2: 인증서 가져오기
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

이 명령은 MyUserCertificate 이라는 인증서를 가져옵니다.

## 변수

### -AutomationAccountName
인증서를 사용 하 여 automation 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
검색할 인증서의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft. Azure. CertificateInfo

## 상속자

## 관련 링크

[새-AzureAutomationCertificate](./New-AzureAutomationCertificate.md)

[-AzureAutomationCertificate 제거](./Remove-AzureAutomationCertificate.md)

[Set-AzureAutomationCertificate](./Set-AzureAutomationCertificate.md)


