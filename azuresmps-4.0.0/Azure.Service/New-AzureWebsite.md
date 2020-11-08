---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046184"
---
# New-AzureWebsite

## SYNOPSIS
Azure에서 실행할 새 웹 사이트를 만듭니다.

## 구문과

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

Cmdlet은 Azure에서 실행할 새 웹 사이트를 만들고 Github를 통해 배포를 준비 합니다.

## 예제의

### 예제 1: Git을 사용 하 여 새 웹 사이트 만들기
```
PS C:\> New-AzureWebsite mySite -Git
```

이 예제에서는 Azure에 새 웹 사이트를 만들고 새 웹 사이트에 파일을 배포 하는 데 사용할 로컬 Git 리포지토리를 만듭니다.

### 예제 2: Github와 통합 된 웹 사이트 만들기
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

이 예제에서는 내 계정/myrepo 이라는 Github 리포지토리에 연결 된 새 웹 사이트를 만듭니다.
Github 리포지토리에 대 한 커밋이 Azure의 웹 사이트로 푸시됩니다.

## 변수

### -Git
로컬 Git 리포지토리를 설정 하 고 웹 사이트에 연결 합니다.
지정 하는 경우이 매개 변수는 로컬 디렉터리에 Git 리포지토리를 설정 하 고 Azure의 웹 사이트에 연결 되는 ' azure ' 라는 원격 리포지토리를 추가 합니다.

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
이 cmdlet이 새 웹 사이트를 기존 Github 리포지토리에 연결 하는 것을 나타냅니다.
Giuthub 저장소에 대 한 커밋이 Azure의 웹 사이트로 푸시됩니다.

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

### -Gid 자격 증명
Github에 연결 하는 데 사용 되는 사용자 이름 및 암호 자격 증명을 지정 합니다.

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

### -GithubRepository
이 웹 사이트에 연결할 Github 리포지토리의 전체 이름을 지정 합니다.
예를 들어 `myaccount/myrepo` .

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
새 웹 사이트의 대체 호스트 이름을 지정 합니다.

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

### -위치
웹 사이트를 배포 하려는 데이터 센터의 위치를 지정 합니다.

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

### -이름
웹 사이트의 이름을 지정 합니다.

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

### -PublishingUsername
Git 배포용 Azure 포털에서 지정한 사용자 이름을 지정 합니다.

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

### -슬롯
웹 사이트의 슬롯 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Set-AzureWebsite](./Set-AzureWebsite.md)


