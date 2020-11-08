---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046274"
---
# Get-AzureWebsite

## SYNOPSIS
현재 구독에서 Azure 웹 사이트를 가져옵니다.

## 구문과

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureWebsite** cmdlet은 현재 구독의 Azure websites에 대 한 정보를 가져옵니다.

기본적으로 **Get-AzureWebsite** 는 현재 구독의 모든 Azure 웹 사이트를 가져오며 사이트에 대 한 기본 정보를 제공 하는 개체를 반환 합니다.
*Name* 매개 변수를 사용 하는 경우 **Get-AzureWebsite** 는 구성 세부 정보를 포함 하 여 자세한 정보가 포함 된 개체를 반환 합니다.

현재 구독은 "current"로 지정 된 구독입니다. 현재 구독을 찾으려면 [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) Cmdlet의 *현재* 매개 변수를 사용 합니다.
현재 구독을 변경 하려면 [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet을 사용 합니다.

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 구독에 있는 모든 웹 사이트 가져오기
```
PS C:\> Get-AzureWebsite
```

이 명령은 현재 구독에 있는 모든 Azure 웹 사이트를 가져옵니다.

### 예제 2: 이름으로 웹 사이트 가져오기
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

이 명령은 구성 정보를 포함 하 여 ContosoWeb Azure 웹 사이트에 대 한 자세한 정보를 가져옵니다.
*Name* 매개 변수를 사용 하는 경우 **Get-AzureWebsite** 는 웹 사이트에 대 한 확장 정보가 있는 **sitewithconfig** 개체를 반환 합니다.

### 예제 3: 모든 웹사이트에 대 한 자세한 정보 보기
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

이 명령은 구독의 모든 웹사이트에 대 한 자세한 정보를 가져옵니다.
**AzureWebsite** 명령을 사용 하 여 모든 웹 사이트를 가져와 **ForEach-개체** cmdlet을 사용 하 여 각 웹 사이트를 이름으로 가져옵니다.

### 예제 4: 배포 슬롯에 대 한 정보 가져오기
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

이 명령은 ContosoWeb 웹 사이트의 스테이징 배포 슬롯을 가져옵니다.
배포 슬롯을 사용 하면 다른 버전의 Azure 웹 사이트를 공개 하지 않고 테스트할 수 있습니다.

### 예제 5: 웹 사이트 인스턴스 가져오기
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

이 예제의 명령은 Azure 웹 사이트의 Instances 속성을 사용 하 여 현재 실행 중인 웹 사이트 인스턴스에 대 한 정보를 가져옵니다.
**인스턴스** 속성은 Azure 모듈 버전 0.8.3의 **sitewithconfig** 개체에 추가 되었습니다.

첫 번째 명령은 현재 웹 사이트에서 실행 중인 모든 인스턴스의 인스턴스 Id를 가져옵니다.
두 번째 명령은 웹 사이트의 실행 중인 인스턴스 수를 가져옵니다.
모든 배열에서 **Count** 속성을 사용할 수 있습니다.

## 변수

### -이름
지정 된 웹 사이트에 대 한 자세한 구성 정보를 가져옵니다.
구독에 한 웹 사이트의 이름을 입력 합니다.
기본적으로 **Get-AzureWebsite** 는 현재 구독에 있는 모든 웹 사이트를 가져옵니다.
*Name* 값은 와일드 카드 문자를 지원 하지 않습니다.

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

### -슬롯
웹 사이트의 지정 된 배포 슬롯을 가져옵니다.
슬롯 이름 (예: "준비" 또는 "생산")을 입력 합니다.
배포 슬롯에 대 한 자세한 내용은 Microsoft Azure 웹 사이트의 단계적 배포를 참조 https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ 하세요.
기존 Azure 웹 사이트에 배포 슬롯을 추가 하려면 Set-AzureWebsite cmdlet을 사용 합니다.

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

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### WindowsAzure. *. * WebEntities. Site
기본적으로 **Get-AzureWebsite** 는 **사이트** 개체의 배열을 반환 합니다.

### WindowsAzure. 유틸리티. a i m/WebEntities. SiteWithConfig
*Name* 매개 변수를 사용 하는 경우 **Get-AzureWebsite** 는 **sitewithconfig** 개체를 반환 합니다.

## 상속자

## 관련 링크

[새로운 AzureWebsite](./New-AzureWebsite.md)

[제거-AzureWebsite](./Remove-AzureWebsite.md)

[시작-AzureWebsite](./Start-AzureWebsite.md)

[중지-AzureWebsite](./Stop-AzureWebsite.md)

[쇼-AzureWebsite](./Show-AzureWebsite.md)


