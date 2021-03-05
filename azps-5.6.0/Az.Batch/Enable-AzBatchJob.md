---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 1470f02570462a3a7bb922c88504e3c8a20eb8fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971563"
---
# <span data-ttu-id="571c1-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="571c1-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="571c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="571c1-102">SYNOPSIS</span></span>
<span data-ttu-id="571c1-103">Batch 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-103">Enables a Batch job.</span></span>

## <span data-ttu-id="571c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="571c1-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="571c1-105">설명</span><span class="sxs-lookup"><span data-stu-id="571c1-105">DESCRIPTION</span></span>
<span data-ttu-id="571c1-106">**Enable-AzBatchJob** cmdlet을 사용하면 Azure Batch 작업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="571c1-107">작업을 사용하도록 설정한 후 새 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="571c1-108">예제</span><span class="sxs-lookup"><span data-stu-id="571c1-108">EXAMPLES</span></span>

### <span data-ttu-id="571c1-109">예제 1: Batch 작업 사용</span><span class="sxs-lookup"><span data-stu-id="571c1-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="571c1-110">이 명령을 사용하면 ID Job-000001이 있는 작업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="571c1-111">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="571c1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="571c1-112">PARAMETERS</span></span>

### <span data-ttu-id="571c1-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="571c1-113">-BatchContext</span></span>
<span data-ttu-id="571c1-114">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="571c1-115">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="571c1-116">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="571c1-117">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="571c1-118">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="571c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571c1-119">-DefaultProfile</span></span>
<span data-ttu-id="571c1-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="571c1-121">-Id</span><span class="sxs-lookup"><span data-stu-id="571c1-121">-Id</span></span>
<span data-ttu-id="571c1-122">이 cmdlet에서 사용 가능하게 하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="571c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571c1-123">CommonParameters</span></span>
<span data-ttu-id="571c1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="571c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571c1-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="571c1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571c1-126">입력</span><span class="sxs-lookup"><span data-stu-id="571c1-126">INPUTS</span></span>

### <span data-ttu-id="571c1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="571c1-127">System.String</span></span>

### <span data-ttu-id="571c1-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="571c1-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="571c1-129">출력</span><span class="sxs-lookup"><span data-stu-id="571c1-129">OUTPUTS</span></span>

### <span data-ttu-id="571c1-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="571c1-130">System.Void</span></span>

## <span data-ttu-id="571c1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="571c1-131">NOTES</span></span>

## <span data-ttu-id="571c1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="571c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="571c1-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="571c1-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="571c1-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="571c1-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="571c1-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="571c1-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="571c1-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="571c1-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="571c1-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="571c1-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="571c1-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="571c1-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
