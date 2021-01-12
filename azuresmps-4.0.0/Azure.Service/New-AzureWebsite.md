---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110481"
---
# New-AzureWebsite

## SYNOPSIS
Azure에서 실행할 새 웹 사이트를 만들 수 있습니다.

## 구문

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명
이 항목에서는 Microsoft Azure PowerShell 모듈의 0.8.10 버전 cmdlet에 대해 설명합니다.
사용 하는 모듈의 버전을 얻습니다. Azure PowerShell 콘솔에서 를 `(Get-Module -Name Azure).Version` 입력합니다.

cmdlet은 Azure에서 실행할 새 웹 사이트를 만들고 GitHub를 통해 배포를 준비합니다.

## 예제

### 예제 1: Git를 사용하여 새 웹 사이트 만들기
```
PS C:\> New-AzureWebsite mySite -Git
```

이 예제에서는 새 웹 사이트에 파일을 배포하는 데 사용할 Azure 및 로컬 Git 리포지토리에 새 웹 사이트를 만듭니다.

### 예제 2: GitHub와 통합된 웹 사이트 만들기
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

이 예제에서는 myaccount/myrepo라는 GitHub 리포지토리에 연결된 새 웹 사이트를 만듭니다.
GitHub 리포지토리에 대한 커밋은 Azure의 웹 사이트로 푸시됩니다.

## PARAMETERS

### -Git
로컬 Git 리포지토리를 설정하고 웹 사이트에 연결합니다.
지정된 경우 이 매개 변수는 로컬 디렉터리에서 Git 리포지토리를 설정하고 Azure의 웹 사이트에 연결되는 'azure'라는 원격 리포지토리를 추가합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
이 cmdlet은 새 웹 사이트를 기존 GitHub 리포지토리에 연결합니다.
Giuthub 리포지토리에 대한 커밋은 Azure의 웹 사이트로 푸시됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubCredentials
GitHub에 연결할 사용자 이름 및 암호 자격 증명을 지정합니다.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubRepository
이 웹 사이트에 연결하기 위해 GitHub 리포지토리의 전체 이름을 지정합니다.
예: `myaccount/myrepo`

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

### -Hostname
새 웹 사이트의 대체 호스트 이름을 지정합니다.

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

### -Location
웹 사이트를 배포하려는 데이터 센터의 위치를 지정합니다.

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

### -Name
웹 사이트의 이름을 지정합니다.

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

### -Profile
이 cmdlet이 읽을 Azure 프로필을 지정합니다.
프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.

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

### -PublishingUsername
Git 배포용 Azure Portal에서 지정한 사용자 이름을 지정합니다.

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

### -Slot
웹 사이트의 슬롯 이름을 지정합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

## 출력

## 참고 사항

## 관련 링크

[Set-AzureWebsite](./Set-AzureWebsite.md)


