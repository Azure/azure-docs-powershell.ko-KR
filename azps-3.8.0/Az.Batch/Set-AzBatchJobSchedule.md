---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042425"
---
# <span data-ttu-id="99027-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="99027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99027-102">SYNOPSIS</span></span>
<span data-ttu-id="99027-103">작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-103">Sets a job schedule.</span></span>

## <span data-ttu-id="99027-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99027-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99027-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99027-105">DESCRIPTION</span></span>
<span data-ttu-id="99027-106">**AzBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="99027-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99027-107">EXAMPLES</span></span>

### <span data-ttu-id="99027-108">예제 1: 작업 일정 업데이트</span><span class="sxs-lookup"><span data-stu-id="99027-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="99027-109">첫 번째 명령은 **Get-AzBatchJobSchedule** 를 사용 하 여 작업을 가져온 다음 $JobSchedule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="99027-110">두 번째 명령은 개체의 되풀이 간격을 수정 합니다 `$JobSchedule.Schedule` .</span><span class="sxs-lookup"><span data-stu-id="99027-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="99027-111">마지막 명령은 $JobSchedule의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="99027-112">변수</span><span class="sxs-lookup"><span data-stu-id="99027-112">PARAMETERS</span></span>

### <span data-ttu-id="99027-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99027-113">-BatchContext</span></span>
<span data-ttu-id="99027-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99027-115">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99027-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99027-116">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99027-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99027-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99027-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99027-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99027-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99027-119">-DefaultProfile</span></span>
<span data-ttu-id="99027-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99027-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99027-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-121">-JobSchedule</span></span>
<span data-ttu-id="99027-122">작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="99027-123">**Pscloudjobschedule** 개체를 얻으려면 Get-AzBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="99027-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99027-124">CommonParameters</span></span>
<span data-ttu-id="99027-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99027-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99027-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99027-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99027-127">입력</span><span class="sxs-lookup"><span data-stu-id="99027-127">INPUTS</span></span>

### <span data-ttu-id="99027-128">Microsoft.Azure.Commands.Batch. PSCloudJobSchedule 모델</span><span class="sxs-lookup"><span data-stu-id="99027-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="99027-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99027-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="99027-130">출력</span><span class="sxs-lookup"><span data-stu-id="99027-130">OUTPUTS</span></span>

### <span data-ttu-id="99027-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="99027-131">System.Void</span></span>

## <span data-ttu-id="99027-132">상속자</span><span class="sxs-lookup"><span data-stu-id="99027-132">NOTES</span></span>

## <span data-ttu-id="99027-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99027-133">RELATED LINKS</span></span>

[<span data-ttu-id="99027-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="99027-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="99027-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="99027-137">새로운 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="99027-138">제거-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="99027-139">중지-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99027-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


