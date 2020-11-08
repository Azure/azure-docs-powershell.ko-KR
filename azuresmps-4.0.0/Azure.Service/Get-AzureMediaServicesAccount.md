---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046335"
---
# Get-AzureMediaServicesAccount

## SYNOPSIS
사용할 수 있는 Azure Media 서비스 계정을 가져옵니다.

**참고:** 이 버전은 더 이상 사용 되지 않습니다. [최신 버전](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)을 확인 하세요.

## 구문과

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

모든 계정을 나열 하려면 cmdlet을 사용 `Get-AzureMediaServicesAccount` 합니다.
특정 계정에 대 한 자세한 정보를 보려면 cmdlet을 사용 `Get-AzureMediaServicesAccount -Name YourAccountName` 합니다.

## 예제의

### 예제 1: 모든 미디어 서비스 계정 나열
```
PS C:\> Get-AzureMediaServicesAccount
```

이 명령은 사용 가능한 모든 미디어 서비스 계정을 나열 합니다.

### 예제 2: 미디어 서비스 계정에 대 한 자세한 정보 가져오기
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

이 명령은 미디어 서비스 계정의 속성을 표시 합니다.

## 변수

### -이름
미디어 서비스 계정 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

## 상속자

## 관련 링크

[미디어 서비스에 Azure PowerShell을 사용 하는 방법](https://go.microsoft.com/fwlink/?LinkId=324179)


