---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046512"
---
# Get-AzureWebHostingPlan

## SYNOPSIS
현재 구독에서 Azure 웹 호스팅 계획을 가져옵니다.

## 구문과

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**AzureWebHostingPlan** cmdlet은 현재 구독에서 Azure 웹 호스팅 계획을 가져옵니다.

기본적으로 **Get-AzureWebHostingPlan** 는 현재 구독의 모든 Azure 호스팅 계획을 가져오며 계획에 대 한 기본 정보를 제공 하는 개체를 반환 합니다.
*웹 공간* 및 *이름* 매개 변수를 사용 하는 경우 **Get-AzureWebHostingPlan** 는 특정 호스팅 계획 개체를 반환 합니다.

현재 구독을 찾으려면 **Get-AzureSubscription** Cmdlet의 *현재* 매개 변수를 사용 합니다.
현재 구독을 변경 하려면 **Select-AzureSubscription** cmdlet을 사용 합니다.

## 예제의

### 예제 1: 구독에서 모든 웹 호스팅 계획 가져오기
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

이 명령은 현재 구독에서 모든 Azure 웹 호스팅 계획을 가져옵니다.

### 예제 2: 구독에서 특정 웹 호스팅 계획 가져오기
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

이 명령은 현재 구독의 westeuropewebspace 이라는 웹 공간에서 Default0 이라는 웹 호스팅 계획을 가져옵니다.

## 변수

### -이름
구독에 대 한 계획의 이름을 지정 합니다.
기본적으로이 cmdlet은 현재 구독에 있는 모든 계획을 가져옵니다.
이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.

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

### -WebSpaceName
구독에 있는 웹 스페이스의 이름을 지정 합니다.
기본적으로이 cmdlet은 지정 된 웹 공간에 있는 모든 웹 사이트를 가져옵니다.
이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

###  
속성 이름으로이 cmdlet에 대 한 입력을 전달할 수 있지만 값을 기준으로 하지는 않습니다.

## 출력

### WindowsAzure. WebHostingPlan에 대 한 유틸리티.
기본적으로 **Get-AzureWebHostingPlan** 는 **WebHostingPlan** 개체의 배열을 반환 합니다.

## 상속자

## 관련 링크

