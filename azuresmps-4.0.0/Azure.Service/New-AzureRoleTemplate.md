---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045992"
---
# New-AzureRoleTemplate

## SYNOPSIS
웹 및 작업자 역할 템플릿을 만듭니다.

## 구문과

### WebRole
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 역할
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**새 AzureRoleTemplate** cmdlet은 웹 및 작업자 역할 템플릿을 만듭니다.

## 예제의

### 예제 1: 웹 역할 서식 파일 만들기
```
PS C:\> New-AzureRoleTemplate -Web
```

이 예제에서는 현재 디렉터리에 WebRoleTemplate 이라는 폴더에 새 웹 역할 템플릿을 만듭니다.

### 예제 2: 작업자 역할 템플릿 만들기
```
PS C:\> New-AzureRoleTemplate -Worker
```

이 예제에서는 현재 디렉터리의 WebRoleTemplate 이라는 폴더에 새 작업자 역할 템플릿을 만듭니다.

### 예제 3: 사용자 지정 디렉터리에 역할 서식 파일 만들기
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

이 예제에서는 현재 디렉토리가 아닌 MyWebRoleTemplate 이라는 디렉터리에 새 웹 역할 템플릿을 만듭니다.

## 변수

### -출력
생성 된 템플릿의 출력 경로를 지정 합니다.

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

### -웹
웹 역할 서식 파일을 만들도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Worker
작업자 역할 템플릿을 만들지 여부를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureWebRole](./Add-AzureWebRole.md)

[추가-Azure역할](./Add-AzureWorkerRole.md)


