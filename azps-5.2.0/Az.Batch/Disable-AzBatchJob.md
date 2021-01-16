---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353894"
---
# <span data-ttu-id="dfe13-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfe13-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="dfe13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe13-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe13-103">Batch 작업을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-103">Disables a Batch job.</span></span>

## <span data-ttu-id="dfe13-104">구문</span><span class="sxs-lookup"><span data-stu-id="dfe13-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe13-105">설명</span><span class="sxs-lookup"><span data-stu-id="dfe13-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe13-106">**Disable-AzBatchJob** cmdlet은 Azure Batch 작업을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="dfe13-107">작업을 사용하도록 설정한 후 새 태스크를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="dfe13-108">비활성화된 작업은 새 태스크를 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="dfe13-109">나중에 비활성화된 작업을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="dfe13-110">예제</span><span class="sxs-lookup"><span data-stu-id="dfe13-110">EXAMPLES</span></span>

### <span data-ttu-id="dfe13-111">예제 1: Batch 작업 사용 안</span><span class="sxs-lookup"><span data-stu-id="dfe13-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="dfe13-112">이 명령은 ID Job-000001이 있는 작업을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dfe13-113">이 명령은 작업에 대한 활성 태스크를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="dfe13-114">**Get-AzBatchAccountKey** cmdlet을 사용하여 $Context 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dfe13-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe13-115">PARAMETERS</span></span>

### <span data-ttu-id="dfe13-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dfe13-116">-BatchContext</span></span>
<span data-ttu-id="dfe13-117">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dfe13-118">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dfe13-119">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dfe13-120">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dfe13-121">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dfe13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe13-122">-DefaultProfile</span></span>
<span data-ttu-id="dfe13-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe13-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="dfe13-124">-DisableJobOption</span></span>
<span data-ttu-id="dfe13-125">이 cmdlet이 비활성화하는 작업과 연결된 활성 태스크로 수행할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="dfe13-126">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="dfe13-126">Valid values are:</span></span>
- <span data-ttu-id="dfe13-127">다시 큐</span><span class="sxs-lookup"><span data-stu-id="dfe13-127">Requeue</span></span>
- <span data-ttu-id="dfe13-128">Terminate</span><span class="sxs-lookup"><span data-stu-id="dfe13-128">Terminate</span></span>
- <span data-ttu-id="dfe13-129">대기</span><span class="sxs-lookup"><span data-stu-id="dfe13-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe13-130">-Id</span><span class="sxs-lookup"><span data-stu-id="dfe13-130">-Id</span></span>
<span data-ttu-id="dfe13-131">이 cmdlet에서 사용하지 않도록 설정하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe13-132">CommonParameters</span></span>
<span data-ttu-id="dfe13-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe13-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfe13-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe13-135">입력</span><span class="sxs-lookup"><span data-stu-id="dfe13-135">INPUTS</span></span>

### <span data-ttu-id="dfe13-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dfe13-136">System.String</span></span>

### <span data-ttu-id="dfe13-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dfe13-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dfe13-138">출력</span><span class="sxs-lookup"><span data-stu-id="dfe13-138">OUTPUTS</span></span>

### <span data-ttu-id="dfe13-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="dfe13-139">System.Void</span></span>

## <span data-ttu-id="dfe13-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dfe13-140">NOTES</span></span>

## <span data-ttu-id="dfe13-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfe13-141">RELATED LINKS</span></span>

[<span data-ttu-id="dfe13-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfe13-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="dfe13-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dfe13-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dfe13-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfe13-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="dfe13-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfe13-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="dfe13-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfe13-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="dfe13-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfe13-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="dfe13-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfe13-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
