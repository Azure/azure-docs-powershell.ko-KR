---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012592"
---
# Get-AzConfluentOrganization

## SYNOPSIS
특정 조직 리소스의 속성을 얻습니다.

## 구문

### 목록(기본값)
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### List1
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명
특정 조직 리소스의 속성을 얻습니다.

## 예제

### 예제 1: 구독 아래에 모든 혼성 조직 나열
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

이 명령은 구독 아래에 있는 모든 confluent 조직을 나열합니다.

### 예제 2: 리소스 그룹 아래에 모든 혼성 조직 나열
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

이 명령은 리소스 그룹 아래에 있는 모든 혼성 조직을 나열합니다.

### 예제 3: 이름에 따라 혼성 조직을 얻다
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

이 명령은 이름을 사용하여 confluent 조직을 얻습니다.

### 예제 4: 파이프라인에 따라 confluent 조직을 얻다
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

이 명령은 파이프라인에 따라 confluent 조직을 얻습니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
조직 리소스 이름

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Microsoft Azure 구독 ID

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


INPUTOBJECT <IConfluentIdentity> : ID 매개 변수
  - `[Id <String>]`: 리소스 ID 경로
  - `[OrganizationName <String>]`: 조직 리소스 이름
  - `[ResourceGroupName <String>]`: 리소스 그룹 이름
  - `[SubscriptionId <String>]`: Microsoft Azure 구독 ID

## 관련 링크

