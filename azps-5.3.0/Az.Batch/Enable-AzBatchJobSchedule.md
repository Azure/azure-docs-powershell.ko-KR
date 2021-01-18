---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494170"
---
# <span data-ttu-id="50c07-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50c07-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="50c07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c07-102">SYNOPSIS</span></span>
<span data-ttu-id="50c07-103">Batch 작업 일정을 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="50c07-104">구문</span><span class="sxs-lookup"><span data-stu-id="50c07-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c07-105">설명</span><span class="sxs-lookup"><span data-stu-id="50c07-105">DESCRIPTION</span></span>
<span data-ttu-id="50c07-106">**Enable-AzBatchJobSchedule** cmdlet을 사용하면 Azure Batch 작업 일정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="50c07-107">작업 일정을 사용하도록 설정한 후 해당 일정에 따라 작업을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="50c07-108">예제</span><span class="sxs-lookup"><span data-stu-id="50c07-108">EXAMPLES</span></span>

### <span data-ttu-id="50c07-109">예제 1: 작업 일정 사용</span><span class="sxs-lookup"><span data-stu-id="50c07-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="50c07-110">이 명령은 ID JobSchedule17이 있는 작업 일정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="50c07-111">**Get-AzBatchAccountKey** cmdlet을 사용하여 $Context 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="50c07-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50c07-112">PARAMETERS</span></span>

### <span data-ttu-id="50c07-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50c07-113">-BatchContext</span></span>
<span data-ttu-id="50c07-114">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50c07-115">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="50c07-116">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="50c07-117">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="50c07-118">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="50c07-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c07-119">-DefaultProfile</span></span>
<span data-ttu-id="50c07-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c07-121">-Id</span><span class="sxs-lookup"><span data-stu-id="50c07-121">-Id</span></span>
<span data-ttu-id="50c07-122">이 cmdlet에서 사용 가능하게 하는 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="50c07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c07-123">CommonParameters</span></span>
<span data-ttu-id="50c07-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50c07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c07-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50c07-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c07-126">입력</span><span class="sxs-lookup"><span data-stu-id="50c07-126">INPUTS</span></span>

### <span data-ttu-id="50c07-127">System.String</span><span class="sxs-lookup"><span data-stu-id="50c07-127">System.String</span></span>

### <span data-ttu-id="50c07-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50c07-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="50c07-129">출력</span><span class="sxs-lookup"><span data-stu-id="50c07-129">OUTPUTS</span></span>

### <span data-ttu-id="50c07-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="50c07-130">System.Void</span></span>

## <span data-ttu-id="50c07-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50c07-131">NOTES</span></span>

## <span data-ttu-id="50c07-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50c07-132">RELATED LINKS</span></span>

[<span data-ttu-id="50c07-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50c07-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="50c07-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="50c07-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="50c07-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50c07-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="50c07-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50c07-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="50c07-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50c07-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="50c07-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50c07-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="50c07-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="50c07-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
