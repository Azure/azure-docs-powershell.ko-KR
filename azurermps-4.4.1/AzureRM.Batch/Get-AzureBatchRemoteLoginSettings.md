---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 848f0cf3d2d36b9ff5c80792c23d126956dccfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537888"
---
# Get-AzureBatchRemoteLoginSettings

## SYNOPSIS
계산 노드에 대 한 원격 로그온 설정을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### Id (기본값)
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureBatchRemoteLoginSettings** cmdlet은 가상 컴퓨터 인프라 기반 풀의 계산 노드에 대 한 원격 로그온 설정을 가져옵니다.

## 예제의

### 예제 1: 풀의 모든 노드에 대 한 원격 로그온 설정 가져오기
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

첫 번째 명령은 **AzureRmBatchAccountKeys** 를 사용 하 여 구독에 대 한 선택 키를 포함 하는 일괄 처리 계정 컨텍스트를 가져옵니다.
명령은 다음 명령에 사용할 컨텍스트를 $Context 변수에 저장 합니다.

두 번째 명령은 **Get-AzureBatchComputeNode** 를 사용 하 여 ID ContosoPool를 가진 풀의 각 계산 노드를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 각 컴퓨터 노드를 현재 cmdlet에 전달 합니다.
명령은 각 계산 노드에 대 한 원격 로그온 설정을 가져옵니다.

### 예제 2: 노드에 대 한 원격 로그온 설정 가져오기
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

첫 번째 명령은 구독에 대 한 선택 키를 포함 하는 일괄 처리 계정 컨텍스트를 가져온 다음 $Context 변수에 저장 합니다.

두 번째 명령은 ID ContosoPool를 가진 풀에서 지정 된 ID를 갖는 계산 노드에 대 한 원격 로그온 설정을 가져옵니다.

## 변수

### -BatchContext
이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.
구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.

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

### -ComputeNode
이 cmdlet에서 원격 로그온 설정을 가져오는 계산 노드를 **PSComputeNode** 개체로 지정 합니다.
계산 노드 개체를 가져오려면 Get-AzureBatchComputeNode cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
원격 로그온 설정을 가져올 계산 노드의 ID를 지정 합니다.
이 cmdlet에 대 한 원격 로그온 설정을 가져옵니다.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
가상 컴퓨터를 포함 하는 풀의 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### BatchAccountContext
' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.

### PSComputeNode
' ComputeNode ' 매개 변수는 파이프라인에서 ' PSComputeNode ' 형식의 값을 허용 합니다.

## 출력

### PSRemoteLoginSettings

## 상속자

## 관련 링크

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[Get-AzureBatchRemoteDesktopProtocolFile](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[Azure Batch Cmdlet](./AzureRM.Batch.md)


