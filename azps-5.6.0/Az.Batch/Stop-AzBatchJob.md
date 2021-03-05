---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: 43ec21e3c2bb7a0f80dc14c8051e4c3fed20ac42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015515"
---
# <span data-ttu-id="b8c87-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8c87-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="b8c87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c87-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c87-103">Batch 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-103">Stops a Batch job.</span></span>

## <span data-ttu-id="b8c87-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8c87-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c87-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8c87-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c87-106">**Stop-AzBatchJob** cmdlet은 Azure Batch 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="b8c87-107">이 명령은 작업을 완료된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="b8c87-108">예제</span><span class="sxs-lookup"><span data-stu-id="b8c87-108">EXAMPLES</span></span>

### <span data-ttu-id="b8c87-109">예제 1: Batch 작업 중지</span><span class="sxs-lookup"><span data-stu-id="b8c87-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="b8c87-110">이 명령은 ID Job-0000001이 있는 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b8c87-111">명령은 작업을 중지하기로 선택한 이유를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="b8c87-112">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b8c87-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8c87-113">PARAMETERS</span></span>

### <span data-ttu-id="b8c87-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b8c87-114">-BatchContext</span></span>
<span data-ttu-id="b8c87-115">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b8c87-116">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b8c87-117">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b8c87-118">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b8c87-119">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b8c87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c87-120">-DefaultProfile</span></span>
<span data-ttu-id="b8c87-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c87-122">-Id</span><span class="sxs-lookup"><span data-stu-id="b8c87-122">-Id</span></span>
<span data-ttu-id="b8c87-123">이 cmdlet이 중지하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b8c87-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="b8c87-124">-TerminateReason</span></span>
<span data-ttu-id="b8c87-125">작업을 중지하기로 결정한 이유를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="b8c87-126">이 cmdlet은 이 텍스트를 **작업의 TerminateReason 속성으로** 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c87-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c87-127">CommonParameters</span></span>
<span data-ttu-id="b8c87-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c87-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c87-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8c87-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c87-130">입력</span><span class="sxs-lookup"><span data-stu-id="b8c87-130">INPUTS</span></span>

### <span data-ttu-id="b8c87-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c87-131">System.String</span></span>

### <span data-ttu-id="b8c87-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b8c87-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b8c87-133">출력</span><span class="sxs-lookup"><span data-stu-id="b8c87-133">OUTPUTS</span></span>

### <span data-ttu-id="b8c87-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="b8c87-134">System.Void</span></span>

## <span data-ttu-id="b8c87-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8c87-135">NOTES</span></span>

## <span data-ttu-id="b8c87-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8c87-136">RELATED LINKS</span></span>

[<span data-ttu-id="b8c87-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8c87-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="b8c87-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8c87-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b8c87-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b8c87-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b8c87-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8c87-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b8c87-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8c87-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="b8c87-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8c87-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="b8c87-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8c87-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
