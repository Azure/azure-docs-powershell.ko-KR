---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: ce2a7c6d01af33de585d4ac8adef83d03dbd33bc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047205"
---
# <span data-ttu-id="5db67-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5db67-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="5db67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db67-102">SYNOPSIS</span></span>
<span data-ttu-id="5db67-103">지정 된 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="5db67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5db67-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db67-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5db67-105">DESCRIPTION</span></span>
<span data-ttu-id="5db67-106">**AzBatchPool** cmdlet은 지정 된 Azure 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="5db67-107">*Force* 매개 변수를 사용 하지 않는 경우 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="5db67-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5db67-108">EXAMPLES</span></span>

### <span data-ttu-id="5db67-109">예제 1: 풀 ID를 기준으로 일괄 처리 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="5db67-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="5db67-110">이 명령은 ID MyPool를 사용 하 여 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="5db67-111">삭제 작업을 수행 하기 전에 사용자에 게 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="5db67-112">예제 2: 모든 일괄 처리 풀을 강제 삭제</span><span class="sxs-lookup"><span data-stu-id="5db67-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="5db67-113">이 명령은 모든 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="5db67-114">*Force* 매개 변수가 있으므로 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="5db67-115">변수</span><span class="sxs-lookup"><span data-stu-id="5db67-115">PARAMETERS</span></span>

### <span data-ttu-id="5db67-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5db67-116">-BatchContext</span></span>
<span data-ttu-id="5db67-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5db67-118">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5db67-119">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5db67-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5db67-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5db67-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db67-122">-DefaultProfile</span></span>
<span data-ttu-id="5db67-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5db67-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5db67-124">-Force</span></span>
<span data-ttu-id="5db67-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5db67-126">-Id</span><span class="sxs-lookup"><span data-stu-id="5db67-126">-Id</span></span>
<span data-ttu-id="5db67-127">삭제할 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="5db67-128">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="5db67-129">-확인</span><span class="sxs-lookup"><span data-stu-id="5db67-129">-Confirm</span></span>
<span data-ttu-id="5db67-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db67-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db67-131">-WhatIf</span></span>
<span data-ttu-id="5db67-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db67-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db67-134">CommonParameters</span></span>
<span data-ttu-id="5db67-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db67-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5db67-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db67-137">입력</span><span class="sxs-lookup"><span data-stu-id="5db67-137">INPUTS</span></span>

### <span data-ttu-id="5db67-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5db67-138">System.String</span></span>

### <span data-ttu-id="5db67-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5db67-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5db67-140">출력</span><span class="sxs-lookup"><span data-stu-id="5db67-140">OUTPUTS</span></span>

### <span data-ttu-id="5db67-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="5db67-141">System.Void</span></span>

## <span data-ttu-id="5db67-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5db67-142">NOTES</span></span>

## <span data-ttu-id="5db67-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5db67-143">RELATED LINKS</span></span>

[<span data-ttu-id="5db67-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5db67-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5db67-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5db67-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="5db67-146">새로운 AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5db67-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="5db67-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5db67-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


