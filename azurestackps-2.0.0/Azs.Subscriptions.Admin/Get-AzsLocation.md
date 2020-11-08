---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045131"
---
# Get-AzsLocation

## SYNOPSIS
지정 된 위치를 가져옵니다.

## 구문과

### 목록 (기본값)
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명은
지정 된 위치를 가져옵니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

모든 AzureStack 위치 목록을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -이름
AzureStack 위치입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell

## 출력

### SubscriptionsAdmin. Api20151101. ILocation에 대 한

별칭과

## 상속자

복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.

INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수
  - `[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.
  - `[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.
  - `[Id <String>]`: 리소스 id 경로
  - `[Location <String>]`: AzureStack 위치입니다.
  - `[ManifestName <String>]`: 매니페스트 이름입니다.
  - `[Offer <String>]`: 제안의 이름입니다.
  - `[OfferDelegationName <String>]`: 제안 위임의 이름입니다.
  - `[OperationsStatusName <String>]`: 작업 상태 이름입니다.
  - `[Plan <String>]`: 계획의 이름입니다.
  - `[PlanAcquisitionId <String>]`: 계획 획득 식별자
  - `[Quota <String>]`: 할당량의 이름입니다.
  - `[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.
  - `[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.
  - `[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.
  - `[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.

## 관련 링크

