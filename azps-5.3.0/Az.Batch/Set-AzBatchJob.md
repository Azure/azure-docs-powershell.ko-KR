---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494069"
---
# <span data-ttu-id="acd23-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="acd23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd23-102">SYNOPSIS</span></span>
<span data-ttu-id="acd23-103">Batch 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-103">Updates a Batch job.</span></span>

## <span data-ttu-id="acd23-104">구문</span><span class="sxs-lookup"><span data-stu-id="acd23-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd23-105">설명</span><span class="sxs-lookup"><span data-stu-id="acd23-105">DESCRIPTION</span></span>
<span data-ttu-id="acd23-106">**Set-AzBatchJob** cmdlet은 Azure Batch 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="acd23-107">Get-AzBatchJob cmdlet을 사용하여 **PSCloudJob 개체를** 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="acd23-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용하여 Batch 서비스에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="acd23-109">예제</span><span class="sxs-lookup"><span data-stu-id="acd23-109">EXAMPLES</span></span>

### <span data-ttu-id="acd23-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="acd23-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="acd23-111">첫 번째 명령은 **Get-AzBatchJob을** 사용하여 작업을 구한 다음 $Job 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="acd23-112">두 번째 명령은 기본 개체에 대한 우선 순위 $Job 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="acd23-113">마지막 명령은 Batch 서비스의 로컬 개체와 일치하게 Batch 서비스를 $Job.</span><span class="sxs-lookup"><span data-stu-id="acd23-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="acd23-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd23-114">PARAMETERS</span></span>

### <span data-ttu-id="acd23-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="acd23-115">-BatchContext</span></span>
<span data-ttu-id="acd23-116">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="acd23-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="acd23-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="acd23-119">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="acd23-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="acd23-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd23-121">-DefaultProfile</span></span>
<span data-ttu-id="acd23-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acd23-123">-Job</span><span class="sxs-lookup"><span data-stu-id="acd23-123">-Job</span></span>
<span data-ttu-id="acd23-124">이 cmdlet이 Batch 서비스를 업데이트하는 **PSCloudJob을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acd23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd23-125">CommonParameters</span></span>
<span data-ttu-id="acd23-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="acd23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd23-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acd23-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd23-128">입력</span><span class="sxs-lookup"><span data-stu-id="acd23-128">INPUTS</span></span>

### <span data-ttu-id="acd23-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="acd23-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="acd23-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="acd23-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="acd23-131">출력</span><span class="sxs-lookup"><span data-stu-id="acd23-131">OUTPUTS</span></span>

### <span data-ttu-id="acd23-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="acd23-132">System.Void</span></span>

## <span data-ttu-id="acd23-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="acd23-133">NOTES</span></span>

## <span data-ttu-id="acd23-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acd23-134">RELATED LINKS</span></span>

[<span data-ttu-id="acd23-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="acd23-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="acd23-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="acd23-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="acd23-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="acd23-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="acd23-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="acd23-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="acd23-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="acd23-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="acd23-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
