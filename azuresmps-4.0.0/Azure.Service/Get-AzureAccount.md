---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045676"
---
# Get-AzureAccount

## SYNOPSIS
Azure PowerShell에 사용할 수 있는 Azure 계정을 가져옵니다.

## 구문과

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get AzureAccount** Cmdlet은 Windows PowerShell에서 사용할 수 있는 Azure 계정을 가져옵니다.
Windows PowerShell에서 계정을 사용할 수 있게 하려면 **추가-AzureAccount** 또는 **가져오기-# 파일** cmdlet을 사용 합니다.

## 예제의

### 예제 1: 모든 계정 가져오기
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

이 명령은 지정 된 사용자와 연결 된 모든 계정을 가져옵니다.

### 예제 2: 이름으로 계정 가져오기
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

이 명령은 ContosoAdmin 계정을 가져옵니다.

## 변수

### -이름
지정 된 계정만 가져옵니다.
기본값은 Windows PowerShell에서 사용할 수 있는 모든 계정입니다.
계정 이름을 입력 합니다.
**이름** 값은 대/소문자를 구분 합니다.
와일드 카드는 허용 되지 않습니다.

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
이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.

## 출력

### 않아야
이 cmdlet은 출력을 반환 하지 않습니다.

## 상속자

## 관련 링크

[추가-AzureAccount](./Add-AzureAccount.md)

[Get-Azure도움말 파일](./Get-AzurePublishSettingsFile.md)

[가져오기-Azure# settingsfile](./Import-AzurePublishSettingsFile.md)

[-AzureAccount 제거](./Remove-AzureAccount.md)


