---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537768"
---
# New-AzureBatchJob

## SYNOPSIS
일괄 처리 서비스에 작업을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새-AzureBatchJob** Cmdlet은 *batchaccountcontext* 매개 변수에 지정 된 계정의 Azure 일괄 처리 서비스에서 작업을 만듭니다.

## 예제의

### 예제 1: 작업 만들기
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

첫 번째 명령은 New-Object cmdlet을 사용 하 여 **PSPoolInformation** 개체를 만듭니다.
명령이 $PoolInformation 변수에 해당 개체를 저장 합니다.

두 번째 명령은 $PoolInformation에 있는 개체의 **PoolId** 속성에 ID Pool22를 할당 합니다.

마지막 명령은 ID ContosoJob35를 가진 작업을 만듭니다.
작업에 추가 된 작업은 ID Pool22를 가진 풀에서 실행 됩니다.
Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.

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

### -CommonEnvironmentSettings
이 cmdlet이 작업의 모든 작업에 대해 설정 하는 공통 환경 변수를 키/값 쌍으로 지정 합니다.
키는 환경 변수 이름입니다.
값은 환경 변수 값입니다.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -제약 조건
작업에 대 한 실행 제약 조건을 지정 합니다.

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
작업의 표시 이름을 지정 합니다.

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
작업에 대 한 ID를 지정 합니다.

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

### -JobManagerTask
작업 관리자 작업을 지정 합니다.
작업이 시작 되 면 일괄 처리 서비스가 작업 관리자 작업을 실행 합니다.

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobPreparationTask
작업 준비 작업을 지정 합니다.
일괄 처리 서비스는 계산 노드에서 작업 준비 작업을 실행 한 후 해당 작업의 계산 노드에서 작업을 시작 합니다.

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobReleaseTask
작업 릴리스 작업을 지정 합니다.
일괄 처리 서비스는 작업이 종료 될 때 작업 릴리스 작업을 실행 합니다.
일괄 처리 서비스는 작업의 작업을 실행 한 각 계산 노드에서 작업 릴리스 작업을 실행 합니다.

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
작업에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.
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

### -OnAllTasksComplete
작업의 모든 작업이 완료 됨 상태인 경우 일괄 처리 서비스에서 수행 하는 작업을 지정 합니다.

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnTaskFailure
작업의 작업이 실패 하는 경우 일괄 처리 서비스에서 수행 하는 작업을 지정 합니다.

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolInformation
일괄 처리 서비스가 작업의 작업을 실행 하는 풀의 세부 정보를 지정 합니다.

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -우선 순위
작업의 우선 순위를 지정 합니다.
유효한 값은-1000에서 1000 까지의 정수입니다.
값-1000은 가장 낮은 우선 순위입니다.
1000의 값은 가장 높은 우선 순위입니다.
기본값은 0입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsesTaskDependencies
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

[Disable-AzureBatchJob](./Disable-AzureBatchJob.md)

[Enable-AzureBatchJob](./Enable-AzureBatchJob.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[가져오기-AzureBatchJob](./Get-AzureBatchJob.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[-AzureBatchJob 제거](./Remove-AzureBatchJob.md)

[중지-AzureBatchJob](./Stop-AzureBatchJob.md)

[Azure Batch Cmdlet](./AzureRM.Batch.md)


