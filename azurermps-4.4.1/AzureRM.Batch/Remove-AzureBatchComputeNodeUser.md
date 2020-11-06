---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534176"
---
# <span data-ttu-id="27dcb-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="27dcb-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="27dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="27dcb-103">일괄 처리 계산 노드에서 사용자 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27dcb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27dcb-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27dcb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="27dcb-106">**AzureBatchComputeNodeUser** Cmdlet은 Azure Batch compute 노드에서 사용자 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="27dcb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27dcb-107">EXAMPLES</span></span>

### <span data-ttu-id="27dcb-108">예제 1: 확인 하지 않고 계산 노드에서 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="27dcb-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="27dcb-109">이 명령은 ComputeNode01 이라는 계산 노드에서 User14 이라는 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="27dcb-110">계산 노드는 Pool01 라는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="27dcb-111">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="27dcb-112">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="27dcb-113">변수</span><span class="sxs-lookup"><span data-stu-id="27dcb-113">PARAMETERS</span></span>

### <span data-ttu-id="27dcb-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="27dcb-114">-BatchContext</span></span>
<span data-ttu-id="27dcb-115">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27dcb-116">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="27dcb-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="27dcb-117">-ComputeNodeId</span></span>
<span data-ttu-id="27dcb-118">이 cmdlet이 사용자 계정을 삭제 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27dcb-119">-이름</span><span class="sxs-lookup"><span data-stu-id="27dcb-119">-Name</span></span>
<span data-ttu-id="27dcb-120">삭제할 사용자 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="27dcb-121">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-121">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27dcb-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="27dcb-122">-PoolId</span></span>
<span data-ttu-id="27dcb-123">사용자 계정을 삭제할 계산 노드가 포함 된 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27dcb-124">-확인</span><span class="sxs-lookup"><span data-stu-id="27dcb-124">-Confirm</span></span>
<span data-ttu-id="27dcb-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27dcb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27dcb-126">-WhatIf</span></span>
<span data-ttu-id="27dcb-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27dcb-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27dcb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dcb-129">-DefaultProfile</span></span>
<span data-ttu-id="27dcb-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27dcb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dcb-131">CommonParameters</span></span>
<span data-ttu-id="27dcb-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dcb-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27dcb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dcb-134">입력</span><span class="sxs-lookup"><span data-stu-id="27dcb-134">INPUTS</span></span>

### <span data-ttu-id="27dcb-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27dcb-135">BatchAccountContext</span></span>
<span data-ttu-id="27dcb-136">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dcb-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="27dcb-137">출력</span><span class="sxs-lookup"><span data-stu-id="27dcb-137">OUTPUTS</span></span>

## <span data-ttu-id="27dcb-138">상속자</span><span class="sxs-lookup"><span data-stu-id="27dcb-138">NOTES</span></span>

## <span data-ttu-id="27dcb-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27dcb-139">RELATED LINKS</span></span>

[<span data-ttu-id="27dcb-140">새로운 AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="27dcb-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="27dcb-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="27dcb-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="27dcb-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="27dcb-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


