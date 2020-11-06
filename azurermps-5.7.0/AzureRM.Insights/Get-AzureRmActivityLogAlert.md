---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536780"
---
# Get-AzureRmActivityLogAlert

## SYNOPSIS
하나 이상의 활동 로그 알림 리소스를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### GetByNameAndResourceGroup
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureRmActivityLogAlert** cmdlet은 하나 이상의 활동 로그 알림 리소스를 가져옵니다.

## 예제의

### 예제 1: 구독 ID로 활동 로그 알림 가져오기
```
PS C:\>Get-AzureRmActivityLogAlert
```

이 명령은 현재 구독에 대 한 모든 활동 로그 알림을 나열 합니다.

### 예제 2: 지정 된 리소스 그룹에 대 한 활동 로그 알림 가져오기
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

이 명령은 지정 된 리소스 그룹에 대 한 활동 로그 알림을 나열 합니다.

### 예제 3: 활동 로그 알림 가져오기
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

이 명령은 하나 (단일 요소가 있는 목록) 활동 로그 알림을 나열 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
활동 로그 알림의 이름입니다.

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
경고 리소스가 있는 리소스 그룹의 이름입니다.
Name이 null이 아니거나 비어 있지 않은 경우이 매개 변수는 string을 포함 하 고 비어 있어야 합니다.

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
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

## 출력

### <. List ' 1 [Microsoft Azure. e. OutputClasses. PSActivityLogAlertResource]

### 않아야

## 상속자

## 관련 링크

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[업데이트-AzureRmActivityLogAlert](./Update-AzureRmActivityLogAlert.md)

[제거-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[새로운 AzureRmActionGroup](./New-AzureRmActionGroup.md)

[새로운 AzureRmActivityLogAlertCondition](./Get-AzureRmActivityLogAlertCondition.md)
