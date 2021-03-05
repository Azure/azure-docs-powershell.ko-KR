---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 85226072ca3e94a1e9cd10cd5a29e4fbee229c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965147"
---
# <span data-ttu-id="cbe11-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbe11-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="cbe11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe11-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe11-103">Batch 작업 일정을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="cbe11-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbe11-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbe11-105">설명</span><span class="sxs-lookup"><span data-stu-id="cbe11-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe11-106">**Stop-AzBatchJobSchedule** cmdlet은 Azure Batch 작업 일정을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="cbe11-107">예제</span><span class="sxs-lookup"><span data-stu-id="cbe11-107">EXAMPLES</span></span>

### <span data-ttu-id="cbe11-108">예제 1: 작업 일정 중지</span><span class="sxs-lookup"><span data-stu-id="cbe11-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="cbe11-109">이 명령은 ID JobSchedule17이 있는 작업 일정을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cbe11-110">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cbe11-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbe11-111">PARAMETERS</span></span>

### <span data-ttu-id="cbe11-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cbe11-112">-BatchContext</span></span>
<span data-ttu-id="cbe11-113">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cbe11-114">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cbe11-115">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cbe11-116">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cbe11-117">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cbe11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe11-118">-DefaultProfile</span></span>
<span data-ttu-id="cbe11-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbe11-120">-Id</span><span class="sxs-lookup"><span data-stu-id="cbe11-120">-Id</span></span>
<span data-ttu-id="cbe11-121">이 cmdlet이 중지하는 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="cbe11-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe11-122">CommonParameters</span></span>
<span data-ttu-id="cbe11-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe11-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe11-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbe11-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe11-125">입력</span><span class="sxs-lookup"><span data-stu-id="cbe11-125">INPUTS</span></span>

### <span data-ttu-id="cbe11-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cbe11-126">System.String</span></span>

### <span data-ttu-id="cbe11-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cbe11-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cbe11-128">출력</span><span class="sxs-lookup"><span data-stu-id="cbe11-128">OUTPUTS</span></span>

### <span data-ttu-id="cbe11-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="cbe11-129">System.Void</span></span>

## <span data-ttu-id="cbe11-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbe11-130">NOTES</span></span>

## <span data-ttu-id="cbe11-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbe11-131">RELATED LINKS</span></span>

[<span data-ttu-id="cbe11-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbe11-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="cbe11-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbe11-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="cbe11-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cbe11-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cbe11-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbe11-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="cbe11-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbe11-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="cbe11-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbe11-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="cbe11-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbe11-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
