---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: 91ac0d6202eb02f724f3ea17e57846e6db6b7412
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869281"
---
# <span data-ttu-id="a94fb-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="a94fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a94fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a94fb-103">작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-103">Sets a job schedule.</span></span>

## <span data-ttu-id="a94fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a94fb-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a94fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a94fb-105">DESCRIPTION</span></span>
<span data-ttu-id="a94fb-106">**AzBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="a94fb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a94fb-107">EXAMPLES</span></span>

### <span data-ttu-id="a94fb-108">예제 1: 작업 일정 업데이트</span><span class="sxs-lookup"><span data-stu-id="a94fb-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="a94fb-109">첫 번째 명령은 **Get-AzBatchJobSchedule** 를 사용 하 여 작업을 가져온 다음 $JobSchedule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="a94fb-110">두 번째 명령은 개체의 되풀이 간격을 수정 합니다 `$JobSchedule.Schedule` .</span><span class="sxs-lookup"><span data-stu-id="a94fb-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="a94fb-111">마지막 명령은 $JobSchedule의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="a94fb-112">변수</span><span class="sxs-lookup"><span data-stu-id="a94fb-112">PARAMETERS</span></span>

### <span data-ttu-id="a94fb-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a94fb-113">-BatchContext</span></span>
<span data-ttu-id="a94fb-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a94fb-115">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a94fb-116">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a94fb-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a94fb-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a94fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94fb-119">-DefaultProfile</span></span>
<span data-ttu-id="a94fb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a94fb-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-121">-JobSchedule</span></span>
<span data-ttu-id="a94fb-122">작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="a94fb-123">**Pscloudjobschedule** 개체를 얻으려면 Get-AzBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="a94fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94fb-124">CommonParameters</span></span>
<span data-ttu-id="a94fb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94fb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a94fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94fb-127">입력</span><span class="sxs-lookup"><span data-stu-id="a94fb-127">INPUTS</span></span>

### <span data-ttu-id="a94fb-128">Microsoft.Azure.Commands.Batch. PSCloudJobSchedule 모델</span><span class="sxs-lookup"><span data-stu-id="a94fb-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="a94fb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a94fb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a94fb-130">출력</span><span class="sxs-lookup"><span data-stu-id="a94fb-130">OUTPUTS</span></span>

### <span data-ttu-id="a94fb-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a94fb-131">System.Void</span></span>

## <span data-ttu-id="a94fb-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a94fb-132">NOTES</span></span>

## <span data-ttu-id="a94fb-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a94fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="a94fb-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="a94fb-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="a94fb-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="a94fb-137">새로운 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="a94fb-138">제거-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="a94fb-139">중지-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a94fb-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


