---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93701905"
---
# <span data-ttu-id="cf585-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cf585-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="cf585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf585-102">SYNOPSIS</span></span>
<span data-ttu-id="cf585-103">일괄 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-103">Enables a Batch job.</span></span>

## <span data-ttu-id="cf585-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf585-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf585-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cf585-105">DESCRIPTION</span></span>
<span data-ttu-id="cf585-106">AzBatchJob cmdlet을 **사용** 하면 Azure 일괄 작업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="cf585-107">작업을 사용 하도록 설정한 후에는 새 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="cf585-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cf585-108">EXAMPLES</span></span>

### <span data-ttu-id="cf585-109">예제 1: 일괄 처리 작업 사용</span><span class="sxs-lookup"><span data-stu-id="cf585-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="cf585-110">이 명령을 사용 하면 ID 작업이 있는 작업을 000001 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="cf585-111">Get-AzBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cf585-112">변수</span><span class="sxs-lookup"><span data-stu-id="cf585-112">PARAMETERS</span></span>

### <span data-ttu-id="cf585-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf585-113">-BatchContext</span></span>
<span data-ttu-id="cf585-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf585-115">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf585-116">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf585-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf585-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cf585-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf585-119">-DefaultProfile</span></span>
<span data-ttu-id="cf585-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf585-121">-Id</span><span class="sxs-lookup"><span data-stu-id="cf585-121">-Id</span></span>
<span data-ttu-id="cf585-122">이 cmdlet이 사용할 수 있는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="cf585-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf585-123">CommonParameters</span></span>
<span data-ttu-id="cf585-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf585-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf585-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf585-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf585-126">입력</span><span class="sxs-lookup"><span data-stu-id="cf585-126">INPUTS</span></span>

### <span data-ttu-id="cf585-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf585-127">System.String</span></span>

### <span data-ttu-id="cf585-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf585-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cf585-129">출력</span><span class="sxs-lookup"><span data-stu-id="cf585-129">OUTPUTS</span></span>

### <span data-ttu-id="cf585-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="cf585-130">System.Void</span></span>

## <span data-ttu-id="cf585-131">상속자</span><span class="sxs-lookup"><span data-stu-id="cf585-131">NOTES</span></span>

## <span data-ttu-id="cf585-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf585-132">RELATED LINKS</span></span>

[<span data-ttu-id="cf585-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cf585-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="cf585-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cf585-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="cf585-135">새로운 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cf585-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="cf585-136">제거-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cf585-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="cf585-137">중지-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cf585-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="cf585-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf585-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


