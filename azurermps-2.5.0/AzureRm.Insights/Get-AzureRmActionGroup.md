---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883081"
---
# Get-AzureRmActionGroup

## SYNOPSIS
작업 그룹을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### BySubscriptionOrResourceGroup (기본값)
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureRmActionGroup** cmdlet은 하나 이상의 작업 그룹을 가져옵니다.

## 예제의

### 예제 1: 구독 ID를 기준으로 작업 그룹 가져오기
```
PS C:\>Get-AzureRmActionGroup
```

이 명령은 현재 구독에 대 한 모든 작업 그룹을 나열 합니다.

### 예제 2: 지정 된 리소스 그룹에 대 한 작업 그룹 가져오기
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

이 명령은 지정 된 리소스 그룹에 대 한 작업 그룹을 나열 합니다.

### 예제 3: 작업 그룹 가져오기
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

이 명령은 하나 (단일 요소를 포함 하는 목록) 작업 그룹을 나열 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
작업 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
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

### System. 문자열

## 출력

### . Psactiongrou보도 정보 클래스.

## 상속자

## 관련 링크

[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [제거-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [새로운 AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)
