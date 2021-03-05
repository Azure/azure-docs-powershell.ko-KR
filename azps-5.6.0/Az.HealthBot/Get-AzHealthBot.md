---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013232"
---
# Get-AzHealthBot

## SYNOPSIS
HealthBot을 얻습니다.

## 구문

### List1(기본값)
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 목록
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 설명
HealthBot을 얻습니다.

## 예제

### 예제 1: 모든 HealthBot 사용
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

모든 HealthBot을 얻다

### 예제 2: ResourceGroupName에 의해 모든 HealthBot을 얻다
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

ResourceGroupName에 의해 모든 HealthBot을 얻게 됩니다.

### 예제 3: ResourceGroupName 및 Name에 의해 HealthBot을 얻다
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

ResourceGroupName 및 Name에 의해 HealthBot을 얻다

### 예제 4: InputObject로 HealthBot을 얻습니다.
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

InputObject로 HealthBot을 얻습니다.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
봇 리소스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
사용자 구독의 Bot 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 구독 ID입니다.

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

### Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


INPUTOBJECT <IHealthBotIdentity> : ID 매개 변수
  - `[BotName <String>]`: 봇 리소스의 이름입니다.
  - `[Id <String>]`: 리소스 ID 경로
  - `[ResourceGroupName <String>]`: 사용자 구독의 Bot 리소스 그룹의 이름입니다.
  - `[SubscriptionId <String>]`: Azure 구독 ID입니다.

## 관련 링크

