---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181900"
---
# New-AzBotService

## SYNOPSIS
매개 변수로 지정된 BotService를 반환합니다.

## 구문

### 등록(기본값)
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### WebApp
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명
매개 변수로 지정된 BotService를 반환합니다.

## 예제

### 예제 1: 새 봇 만들기
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

ResourceGroupName 및 ApplicationId로 새 봇 만들기

### 예제 2: 새 웹앱 만들기
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

ResourceGroupName 및 ApplicationId로 새 웹앱 만들기

## PARAMETERS

### -ApplicationId


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationSecret


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BotTemplateType


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Description


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExistingServerFarmId


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
봇 리소스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Registration


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
사용자 구독의 봇 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
SKU 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 구독 ID입니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webapp


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot

## 참고 사항

별칭

## 관련 링크

