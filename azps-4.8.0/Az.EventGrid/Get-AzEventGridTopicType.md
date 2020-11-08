---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056356"
---
# Get-AzEventGridTopicType

## SYNOPSIS
Azure 이벤트 표에서 지원 되는 항목 형식에 대 한 세부 정보를 가져옵니다.

## 구문과

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Azure 이벤트 표에서 지원 되는 항목 종류의 세부 정보를 가져옵니다.
주제 형식 이름을 지정 하면 해당 주제 형식에 대 한 세부 정보가 반환 됩니다.
주제 형식 이름을 지정 하지 않으면 모든 항목 종류에 대 한 세부 정보가 반환 됩니다.
IncludeEventTypes가 지정 된 경우 각 항목 유형에 의해 지원 되는 이벤트 유형에 대 한 정보가 응답에 포함 됩니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

항목 형식의 목록을 가져옵니다.

### 예제 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

StorageAccounts 항목 형식에 대 한 정보를 가져옵니다.

### 예제 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

StorageAccounts에서 지원 되는 이벤트 유형을 비롯 하 여 StorageAccounts 주제 유형에 대 한 정보를 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeEventTypeData
지정 되는 경우 응답에는 항목 형식에서 지원 되는 이벤트 형식이 포함 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
EventGrid 주제 형식 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### Microsoft. PSTopicTypeInfoListInstance 표.

### Microsoft. Azure.. m a m. 모델.

## 상속자

## 관련 링크
