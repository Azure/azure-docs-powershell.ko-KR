---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226268"
---
# Get-AzBlockchainTransactionNode

## SYNOPSIS
트랜잭션 노드의 세부 정보를 가져옵니다.

## 구문과

### 목록 (기본값)
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 설명은
트랜잭션 노드의 세부 정보를 가져옵니다.

## 예제의

### 예제 1: blockchain 구성원에 대 한 트랜잭션 노드 나열
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

이 명령은 blockchain 구성원에 대 한 트랜잭션 노드를 나열 합니다.

### 예제 2: 트랜잭션 노드 가져오기
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

이 명령은 트랜잭션 노드를 가져옵니다.

### 예제 3: 트랜잭션 노드 가져오기
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

이 명령은 트랜잭션 노드를 가져옵니다.

## 변수

### -BlockchainMemberName
Blockchain 구성원 이름입니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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
생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
트랜잭션 노드 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스가 포함 된 자원 그룹의 이름입니다.
Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.

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
Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.
구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### IBlockchainIdentity (Microsoft. PowerShell.)

## 출력

### Api20180601Preview. ITransactionNode에 대 한 Microsoft.

## 상속자

별칭과

복합 매개 변수 속성

아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.


INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수
  - `[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.
  - `[Id <String>]`: 리소스 id 경로
  - `[Location <String>]`: 위치 이름입니다.
  - `[OperationId <String>]`: 작업 Id입니다.
  - `[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.
  - `[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.
  - `[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.

## 관련 링크

