---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 59afa8f2ad5b1cf8739bece249d63574c8db6e4c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880110"
---
# <span data-ttu-id="45c1c-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45c1c-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="45c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="45c1c-103">일괄 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="45c1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45c1c-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45c1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="45c1c-106">**AzBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="45c1c-107">일정을 사용 하지 않도록 설정 하면 해당 일정에 따라 작업이 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="45c1c-108">나중에 비활성화 된 일정을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="45c1c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="45c1c-109">EXAMPLES</span></span>

### <span data-ttu-id="45c1c-110">예제 1: 작업 일정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="45c1c-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="45c1c-111">이 명령은 ID JobSchedule17 있는 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="45c1c-112">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-112">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="45c1c-113">변수</span><span class="sxs-lookup"><span data-stu-id="45c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="45c1c-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="45c1c-114">-BatchContext</span></span>
<span data-ttu-id="45c1c-115">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="45c1c-116">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="45c1c-117">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="45c1c-118">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="45c1c-119">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="45c1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c1c-120">-DefaultProfile</span></span>
<span data-ttu-id="45c1c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45c1c-122">-Id</span><span class="sxs-lookup"><span data-stu-id="45c1c-122">-Id</span></span>
<span data-ttu-id="45c1c-123">이 cmdlet이 사용 하지 않도록 설정 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="45c1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c1c-124">CommonParameters</span></span>
<span data-ttu-id="45c1c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c1c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c1c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c1c-127">입력</span><span class="sxs-lookup"><span data-stu-id="45c1c-127">INPUTS</span></span>

### <span data-ttu-id="45c1c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="45c1c-128">System.String</span></span>

### <span data-ttu-id="45c1c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="45c1c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="45c1c-130">출력</span><span class="sxs-lookup"><span data-stu-id="45c1c-130">OUTPUTS</span></span>

### <span data-ttu-id="45c1c-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="45c1c-131">System.Void</span></span>

## <span data-ttu-id="45c1c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="45c1c-132">NOTES</span></span>

## <span data-ttu-id="45c1c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45c1c-133">RELATED LINKS</span></span>

[<span data-ttu-id="45c1c-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45c1c-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="45c1c-135">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="45c1c-135">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="45c1c-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45c1c-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="45c1c-137">새로운 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45c1c-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="45c1c-138">제거-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45c1c-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="45c1c-139">중지-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45c1c-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="45c1c-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="45c1c-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


