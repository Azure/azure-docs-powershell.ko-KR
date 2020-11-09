---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309690"
---
# <span data-ttu-id="dc238-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc238-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="dc238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc238-102">SYNOPSIS</span></span>
<span data-ttu-id="dc238-103">일괄 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-103">Stops a Batch job.</span></span>

## <span data-ttu-id="dc238-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc238-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc238-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc238-105">DESCRIPTION</span></span>
<span data-ttu-id="dc238-106">**AzBatchJob** Cmdlet은 Azure 일괄 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="dc238-107">이 명령은 작업을 완료 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="dc238-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dc238-108">EXAMPLES</span></span>

### <span data-ttu-id="dc238-109">예제 1: 일괄 작업 중지</span><span class="sxs-lookup"><span data-stu-id="dc238-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="dc238-110">이 명령은 ID 작업이 있는 작업을 중지 합니다-000001.</span><span class="sxs-lookup"><span data-stu-id="dc238-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dc238-111">명령은 작업을 중지 하도록 선택한 이유를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="dc238-112">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dc238-113">변수</span><span class="sxs-lookup"><span data-stu-id="dc238-113">PARAMETERS</span></span>

### <span data-ttu-id="dc238-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dc238-114">-BatchContext</span></span>
<span data-ttu-id="dc238-115">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dc238-116">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dc238-117">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dc238-118">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dc238-119">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dc238-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc238-120">-DefaultProfile</span></span>
<span data-ttu-id="dc238-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc238-122">-Id</span><span class="sxs-lookup"><span data-stu-id="dc238-122">-Id</span></span>
<span data-ttu-id="dc238-123">이 cmdlet이 중지 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="dc238-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="dc238-124">-TerminateReason</span></span>
<span data-ttu-id="dc238-125">작업을 중지 하기로 결정 한 이유를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="dc238-126">이 cmdlet은이 텍스트를 작업의 **TerminateReason** 속성으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc238-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc238-127">CommonParameters</span></span>
<span data-ttu-id="dc238-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc238-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc238-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc238-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc238-130">입력</span><span class="sxs-lookup"><span data-stu-id="dc238-130">INPUTS</span></span>

### <span data-ttu-id="dc238-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc238-131">System.String</span></span>

### <span data-ttu-id="dc238-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dc238-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dc238-133">출력</span><span class="sxs-lookup"><span data-stu-id="dc238-133">OUTPUTS</span></span>

### <span data-ttu-id="dc238-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="dc238-134">System.Void</span></span>

## <span data-ttu-id="dc238-135">상속자</span><span class="sxs-lookup"><span data-stu-id="dc238-135">NOTES</span></span>

## <span data-ttu-id="dc238-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc238-136">RELATED LINKS</span></span>

[<span data-ttu-id="dc238-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc238-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="dc238-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc238-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="dc238-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dc238-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dc238-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc238-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="dc238-141">새로운 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc238-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="dc238-142">제거-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc238-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="dc238-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc238-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
