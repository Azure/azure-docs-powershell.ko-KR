---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333741"
---
# <span data-ttu-id="34624-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="34624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34624-102">SYNOPSIS</span></span>
<span data-ttu-id="34624-103">작업 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-103">Sets a job schedule.</span></span>

## <span data-ttu-id="34624-104">구문</span><span class="sxs-lookup"><span data-stu-id="34624-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34624-105">설명</span><span class="sxs-lookup"><span data-stu-id="34624-105">DESCRIPTION</span></span>
<span data-ttu-id="34624-106">**Set-AzBatchJobSchedule** cmdlet은 Azure Batch 서비스에서 작업 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="34624-107">예제</span><span class="sxs-lookup"><span data-stu-id="34624-107">EXAMPLES</span></span>

### <span data-ttu-id="34624-108">예제 1: 작업 일정 업데이트</span><span class="sxs-lookup"><span data-stu-id="34624-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="34624-109">첫 번째 명령은 **Get-AzBatchJobSchedule을** 사용하여 작업을 구한 다음, $JobSchedule 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="34624-110">두 번째 명령은 개체의 반복 간격을 `$JobSchedule.Schedule` 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="34624-111">마지막 명령은 Batch 서비스의 로컬 개체와 일치하게 Batch 서비스를 $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="34624-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="34624-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34624-112">PARAMETERS</span></span>

### <span data-ttu-id="34624-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34624-113">-BatchContext</span></span>
<span data-ttu-id="34624-114">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34624-115">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="34624-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34624-116">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34624-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34624-117">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="34624-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34624-118">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="34624-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34624-119">-DefaultProfile</span></span>
<span data-ttu-id="34624-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34624-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34624-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-121">-JobSchedule</span></span>
<span data-ttu-id="34624-122">작업 일정을 나타내는 **PSCloudJobSchedule** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="34624-123">**PSCloudJobSchedule** 개체를 얻습니다. Get-AzBatchJobSchedule cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34624-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34624-124">CommonParameters</span></span>
<span data-ttu-id="34624-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34624-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34624-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34624-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34624-127">입력</span><span class="sxs-lookup"><span data-stu-id="34624-127">INPUTS</span></span>

### <span data-ttu-id="34624-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="34624-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34624-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="34624-130">출력</span><span class="sxs-lookup"><span data-stu-id="34624-130">OUTPUTS</span></span>

### <span data-ttu-id="34624-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="34624-131">System.Void</span></span>

## <span data-ttu-id="34624-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34624-132">NOTES</span></span>

## <span data-ttu-id="34624-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34624-133">RELATED LINKS</span></span>

[<span data-ttu-id="34624-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="34624-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="34624-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="34624-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="34624-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="34624-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34624-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


