---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: c560964308fe3bb2195f601f2e4138e022aa41e0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880113"
---
# <span data-ttu-id="db380-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="db380-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="db380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db380-102">SYNOPSIS</span></span>
<span data-ttu-id="db380-103">일괄 작업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-103">Disables a Batch job.</span></span>

## <span data-ttu-id="db380-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db380-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db380-105">설명은</span><span class="sxs-lookup"><span data-stu-id="db380-105">DESCRIPTION</span></span>
<span data-ttu-id="db380-106">**AzBatchJob** Cmdlet은 Azure 일괄 작업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="db380-107">작업을 사용 하도록 설정한 후에는 새 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db380-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="db380-108">비활성화 된 작업은 새 작업을 실행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db380-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="db380-109">나중에 비활성화 된 작업을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db380-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="db380-110">예제의</span><span class="sxs-lookup"><span data-stu-id="db380-110">EXAMPLES</span></span>

### <span data-ttu-id="db380-111">예제 1: 일괄 처리 작업 비활성화</span><span class="sxs-lookup"><span data-stu-id="db380-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="db380-112">이 명령은 ID 작업-000001가 있는 작업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="db380-113">명령은 작업에 대 한 활성 작업을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="db380-114">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="db380-115">변수</span><span class="sxs-lookup"><span data-stu-id="db380-115">PARAMETERS</span></span>

### <span data-ttu-id="db380-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="db380-116">-BatchContext</span></span>
<span data-ttu-id="db380-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="db380-118">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db380-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="db380-119">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db380-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="db380-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db380-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="db380-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="db380-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db380-122">-DefaultProfile</span></span>
<span data-ttu-id="db380-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db380-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db380-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="db380-124">-DisableJobOption</span></span>
<span data-ttu-id="db380-125">이 cmdlet이 사용 하지 않도록 설정 하는 작업과 연결 된 활성 작업으로 수행할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="db380-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="db380-126">Valid values are:</span></span> 
- <span data-ttu-id="db380-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="db380-127">Requeue</span></span> 
- <span data-ttu-id="db380-128">종료</span><span class="sxs-lookup"><span data-stu-id="db380-128">Terminate</span></span> 
- <span data-ttu-id="db380-129">Wait</span><span class="sxs-lookup"><span data-stu-id="db380-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db380-130">-Id</span><span class="sxs-lookup"><span data-stu-id="db380-130">-Id</span></span>
<span data-ttu-id="db380-131">이 cmdlet이 사용 하지 않도록 설정할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="db380-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db380-132">CommonParameters</span></span>
<span data-ttu-id="db380-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db380-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db380-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db380-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db380-135">입력</span><span class="sxs-lookup"><span data-stu-id="db380-135">INPUTS</span></span>

### <span data-ttu-id="db380-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db380-136">System.String</span></span>

### <span data-ttu-id="db380-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="db380-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="db380-138">출력</span><span class="sxs-lookup"><span data-stu-id="db380-138">OUTPUTS</span></span>

### <span data-ttu-id="db380-139">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="db380-139">System.Void</span></span>

## <span data-ttu-id="db380-140">상속자</span><span class="sxs-lookup"><span data-stu-id="db380-140">NOTES</span></span>

## <span data-ttu-id="db380-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db380-141">RELATED LINKS</span></span>

[<span data-ttu-id="db380-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="db380-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="db380-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="db380-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="db380-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="db380-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="db380-145">새로운 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="db380-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="db380-146">제거-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="db380-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="db380-147">중지-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="db380-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="db380-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db380-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

