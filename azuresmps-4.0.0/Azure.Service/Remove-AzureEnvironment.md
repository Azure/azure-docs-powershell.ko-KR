---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046477"
---
# Remove-AzureEnvironment

## SYNOPSIS
Windows PowerShell에서 Azure 환경을 삭제 합니다.

## 구문과

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
Windows PowerShell이 로밍 프로필에서 Azure 환경을 찾을 수 없도록 **제거-azureenvironment** cmdlet이 앱을 삭제 합니다.
이 cmdlet은 Microsoft Azure에서 환경을 삭제 하거나 모든 방법으로 실제 환경을 변경 하지는 않습니다.

Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.
Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.
자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## 예제의

### 예제 1: 환경 삭제
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

이 명령은 Windows PowerShell에서 ContosoEnv 환경을 삭제 합니다.

### 예제 2: 여러 환경 삭제
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

이 명령은 이름이 "Contoso"로 시작 하는 환경을 Windows PowerShell에서 삭제 합니다.

## 변수

### -Force
확인 메시지를 표시 하지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
제거할 환경의 이름을 지정 합니다.
이 매개 변수는 필수입니다.
이 매개 변수 값은 대/소문자를 구분 합니다.
와일드 카드 문자는 허용 되지 않습니다.

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

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### 없음 또는 시스템 부울
*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.
그렇지 않으면 출력을 반환 하지 않습니다.

## 상속자

## 관련 링크

[-AzureEnvironment 추가](./Add-AzureEnvironment.md)

[가져오기-AzureEnvironment](./Get-AzureEnvironment.md)

[Set AzureEnvironment](./Set-AzureEnvironment.md)


