---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205405"
---
# <span data-ttu-id="a9493-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a9493-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="a9493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9493-102">SYNOPSIS</span></span>
<span data-ttu-id="a9493-103">Batch 작업 일정을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="a9493-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9493-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9493-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9493-105">DESCRIPTION</span></span>
<span data-ttu-id="a9493-106">**Disable-AzBatchJobSchedule** cmdlet은 Azure Batch 작업 일정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="a9493-107">일정을 사용하지 않도록 설정하면 해당 일정에 따라 작업이 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="a9493-108">나중에 비활성화된 일정을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="a9493-109">예제</span><span class="sxs-lookup"><span data-stu-id="a9493-109">EXAMPLES</span></span>

### <span data-ttu-id="a9493-110">예제 1: 작업 일정 사용 안</span><span class="sxs-lookup"><span data-stu-id="a9493-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="a9493-111">이 명령은 ID JobSchedule17이 있는 작업 일정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="a9493-112">**Get-AzBatchAccountKey** cmdlet을 사용하여 $Context 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a9493-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9493-113">PARAMETERS</span></span>

### <span data-ttu-id="a9493-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a9493-114">-BatchContext</span></span>
<span data-ttu-id="a9493-115">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a9493-116">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a9493-117">대신 공유 키 인증을 사용Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a9493-118">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a9493-119">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a9493-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9493-120">-DefaultProfile</span></span>
<span data-ttu-id="a9493-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9493-122">-Id</span><span class="sxs-lookup"><span data-stu-id="a9493-122">-Id</span></span>
<span data-ttu-id="a9493-123">이 cmdlet이 비활성화하는 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a9493-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9493-124">CommonParameters</span></span>
<span data-ttu-id="a9493-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9493-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9493-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9493-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9493-127">입력</span><span class="sxs-lookup"><span data-stu-id="a9493-127">INPUTS</span></span>

### <span data-ttu-id="a9493-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a9493-128">System.String</span></span>

### <span data-ttu-id="a9493-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a9493-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a9493-130">출력</span><span class="sxs-lookup"><span data-stu-id="a9493-130">OUTPUTS</span></span>

### <span data-ttu-id="a9493-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="a9493-131">System.Void</span></span>

## <span data-ttu-id="a9493-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9493-132">NOTES</span></span>

## <span data-ttu-id="a9493-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9493-133">RELATED LINKS</span></span>

[<span data-ttu-id="a9493-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a9493-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="a9493-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a9493-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a9493-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a9493-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="a9493-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a9493-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="a9493-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a9493-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="a9493-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a9493-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="a9493-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a9493-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
