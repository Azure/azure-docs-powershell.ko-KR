---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357344"
---
# <span data-ttu-id="37747-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="37747-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="37747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37747-102">SYNOPSIS</span></span>
<span data-ttu-id="37747-103">Batch 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="37747-104">구문</span><span class="sxs-lookup"><span data-stu-id="37747-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37747-105">설명</span><span class="sxs-lookup"><span data-stu-id="37747-105">DESCRIPTION</span></span>
<span data-ttu-id="37747-106">**Remove-AzBatchJob** cmdlet은 Azure Batch 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="37747-107">이 cmdlet은 Force 매개 변수를 지정하지 않는 한 작업을 제거하기 전에 확인을 *요청하는 메시지를* 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="37747-108">예제</span><span class="sxs-lookup"><span data-stu-id="37747-108">EXAMPLES</span></span>

### <span data-ttu-id="37747-109">예제 1: Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="37747-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="37747-110">이 명령은 ID Job-000001이 있는 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="37747-111">이 명령은 작업을 삭제하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="37747-112">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="37747-113">예제 2: 파이프라인을 사용하여 확인 없이 Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="37747-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="37747-114">이 명령은 Get-AzBatchJob cmdlet을 사용하여 ID Job-000002가 있는 작업을 Get-AzBatchJob 합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="37747-115">이 명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 작업을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37747-116">이 명령은 해당 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-116">The command deletes that job.</span></span>
<span data-ttu-id="37747-117">이 명령은 Force 매개 *변수를* 포함하기 때문에 확인을 묻는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37747-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="37747-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37747-118">PARAMETERS</span></span>

### <span data-ttu-id="37747-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="37747-119">-BatchContext</span></span>
<span data-ttu-id="37747-120">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="37747-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="37747-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="37747-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="37747-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="37747-123">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="37747-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="37747-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="37747-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37747-125">-DefaultProfile</span></span>
<span data-ttu-id="37747-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37747-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37747-127">-Force</span><span class="sxs-lookup"><span data-stu-id="37747-127">-Force</span></span>
<span data-ttu-id="37747-128">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37747-129">-Id</span><span class="sxs-lookup"><span data-stu-id="37747-129">-Id</span></span>
<span data-ttu-id="37747-130">이 cmdlet이 삭제하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="37747-131">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37747-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="37747-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37747-132">-Confirm</span></span>
<span data-ttu-id="37747-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37747-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37747-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37747-134">-WhatIf</span></span>
<span data-ttu-id="37747-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37747-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37747-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37747-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37747-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37747-137">CommonParameters</span></span>
<span data-ttu-id="37747-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37747-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37747-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37747-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37747-140">입력</span><span class="sxs-lookup"><span data-stu-id="37747-140">INPUTS</span></span>

### <span data-ttu-id="37747-141">System.String</span><span class="sxs-lookup"><span data-stu-id="37747-141">System.String</span></span>

### <span data-ttu-id="37747-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="37747-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="37747-143">출력</span><span class="sxs-lookup"><span data-stu-id="37747-143">OUTPUTS</span></span>

### <span data-ttu-id="37747-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="37747-144">System.Void</span></span>

## <span data-ttu-id="37747-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37747-145">NOTES</span></span>

## <span data-ttu-id="37747-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37747-146">RELATED LINKS</span></span>

[<span data-ttu-id="37747-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="37747-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="37747-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="37747-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="37747-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="37747-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="37747-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="37747-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="37747-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="37747-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="37747-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="37747-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="37747-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37747-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
