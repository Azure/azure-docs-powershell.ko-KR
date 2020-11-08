---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046218"
---
# New-AzureServiceProject

## SYNOPSIS
새 서비스에 필요한 파일과 구성을 만듭니다.

## 구문과

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**새로운-AzureServiceProject** cmdlet은 현재 디렉터리에 새 Azure 서비스에 대 한 필수 파일과 구성을 만듭니다.

## 예제의

### 예제 1: 서비스에 대 한 스 캐 폴딩 만들기
```
PS C:\> New-AzureServiceProject MyService1
```

이 예제에서는 현재 디렉터리에 MyService1 이라는 새 Azure 서비스에 대 한 스 캐 폴딩을 만듭니다.

## 변수

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
서비스의 이름을 지정 합니다.
서비스의 호스트 이름 (예: name.cloudapp.net)과 서비스를 포함 하는 디렉터리의 첫 번째 섹션을 결정 합니다.
이름에는 문자, 숫자 및 대시 문자 (-)만 포함할 수 있습니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[추가-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[게시-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


