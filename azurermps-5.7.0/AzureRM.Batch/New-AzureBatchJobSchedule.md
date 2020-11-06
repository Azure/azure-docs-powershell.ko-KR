---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: a1841fb569cf6ef29bad685679372e0385133568
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537764"
---
# New-AzureBatchJobSchedule

## SYNOPSIS
일괄 처리 서비스에서 작업 일정을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새-AzureBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 만듭니다.
*Batchaccountcontext* 매개 변수는이 cmdlet이 일정을 만드는 계정을 지정 합니다.

## 예제의

### 예제 1: 작업 일정 만들기
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

이 예제에서는 작업 일정을 만듭니다.

처음 5 개 명령은 **Psschedule** , **PSJobSpecification** 및 **PSPoolInformation** 개체를 만들고 수정 합니다.
명령에는 New-Object cmdlet 및 표준 Azure PowerShell 구문이 사용 됩니다.
명령은 $Schedule 및 $JobSpecification 변수에 이러한 개체를 저장 합니다.

마지막 명령은 ID JobSchedule17를 가진 작업 일정을 만듭니다.
이 일정은 되풀이 간격 1 일이 포함 된 작업을 만듭니다.
이 작업은 다섯 번째 명령에 지정 된 대로 ID ContosoPool06가 있는 풀에서 실행 됩니다.
$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.

## 변수

### -BatchContext
이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.
Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다. 대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다. 공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다. 사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -DisplayName
작업 일정의 표시 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
이 cmdlet이 만드는 작업 일정의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobSpecification
작업 일정에이 cmdlet에 포함 된 작업의 세부 정보를 지정 합니다.

```yaml
Type: PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
작업 일정에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.
키는 메타 데이터 이름입니다.
값은 메타 데이터 값입니다.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -일정
작업을 만들 시기를 결정 하는 일정을 지정 합니다.

```yaml
Type: PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### BatchAccountContext
' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.

## 출력

## 상속자

## 관련 링크

[Disable-AzureBatchJobSchedule](./Disable-AzureBatchJobSchedule.md)

[-AzureBatchJobSchedule 사용](./Enable-AzureBatchJobSchedule.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[-AzureBatchJobSchedule 제거](./Remove-AzureBatchJobSchedule.md)

[중지-AzureBatchJobSchedule](./Stop-AzureBatchJobSchedule.md)

[Azure Batch Cmdlet](./AzureRM.Batch.md)


