---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056798"
---
# <span data-ttu-id="ba454-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba454-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="ba454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba454-102">SYNOPSIS</span></span>
<span data-ttu-id="ba454-103">일괄 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="ba454-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba454-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba454-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba454-105">DESCRIPTION</span></span>
<span data-ttu-id="ba454-106">AzBatchJobSchedule cmdlet을 **사용** 하면 Azure Batch 작업 일정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="ba454-107">작업 일정을 사용 하도록 설정한 후에는 해당 일정에 따라 작업을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="ba454-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ba454-108">EXAMPLES</span></span>

### <span data-ttu-id="ba454-109">예제 1: 작업 일정 설정</span><span class="sxs-lookup"><span data-stu-id="ba454-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="ba454-110">이 명령은 ID JobSchedule17가 있는 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="ba454-111">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzBatchAccountKey** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ba454-112">변수</span><span class="sxs-lookup"><span data-stu-id="ba454-112">PARAMETERS</span></span>

### <span data-ttu-id="ba454-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba454-113">-BatchContext</span></span>
<span data-ttu-id="ba454-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba454-115">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba454-116">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba454-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba454-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba454-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba454-119">-DefaultProfile</span></span>
<span data-ttu-id="ba454-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba454-121">-Id</span><span class="sxs-lookup"><span data-stu-id="ba454-121">-Id</span></span>
<span data-ttu-id="ba454-122">이 cmdlet이 사용할 수 있는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="ba454-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba454-123">CommonParameters</span></span>
<span data-ttu-id="ba454-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba454-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba454-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba454-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba454-126">입력</span><span class="sxs-lookup"><span data-stu-id="ba454-126">INPUTS</span></span>

### <span data-ttu-id="ba454-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba454-127">System.String</span></span>

### <span data-ttu-id="ba454-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba454-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba454-129">출력</span><span class="sxs-lookup"><span data-stu-id="ba454-129">OUTPUTS</span></span>

### <span data-ttu-id="ba454-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ba454-130">System.Void</span></span>

## <span data-ttu-id="ba454-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ba454-131">NOTES</span></span>

## <span data-ttu-id="ba454-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba454-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba454-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba454-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="ba454-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba454-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba454-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba454-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="ba454-136">새로운 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba454-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="ba454-137">제거-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba454-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="ba454-138">중지-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba454-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="ba454-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ba454-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
