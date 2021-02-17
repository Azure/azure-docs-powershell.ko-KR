---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197097"
---
# Get-AzBatchSubtask

## SYNOPSIS
지정된 작업의 하위 작업 정보를 얻습니다.

## 구문

### ODataFilter(기본값)
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzBatchSubtask** cmdlet은 지정된 작업에 대한 하위 작업 정보를 검색합니다.
하위 작업은 개별 작업에 대한 병렬 처리를 제공하고 작업 실행 및 진행 상황을 정확하게 모니터링할 수 있도록 합니다.

## 예제

### 예제 1: 지정된 작업에 대한 모든 하위 작업 반환
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

이러한 명령은 id myTask를 사용하여 작업에 대한 모든 하위 작업을 반환합니다.
이를 위해 예제의 첫 번째 명령은 배치 계정 contosobatchaccount에 대한 계정 키에 대한 개체 참조를 만듭니다.
이 개체 참조는 $context.
그런 다음, 두 번째 명령은 해당 개체 참조 및 **Get-AzBatchSubtask** cmdlet을 사용하여 job-01의 일부로 실행되는 태스크인 myTask에 대한 모든 하위 작업을 반환합니다.

## PARAMETERS

### -BatchContext
이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.
Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다. 대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다. 공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다. 사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -JobId
이 cmdlet을 포함하는 하위 작업을 포함하는 작업의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
반환할 하위의 최대 수를 지정합니다.
0 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.
기본값은 1000입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Task
이 cmdlet이 반환하는 하위 작업을 포함하는 작업에 대한 개체 참조를 지정합니다.
이 개체 참조는 Get-AzBatchTask cmdlet을 사용하고 반환된 개체를 변수에 저장하여 만듭니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
이 cmdlet이 반환하는 하위 작업의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## 출력

### Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation

## 참고 사항

## 관련 링크

[Get-AzBatchTask](./Get-AzBatchTask.md)


