---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529939"
---
# <span data-ttu-id="3757e-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3757e-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="3757e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3757e-102">SYNOPSIS</span></span>
<span data-ttu-id="3757e-103">일괄 작업 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3757e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3757e-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3757e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3757e-105">DESCRIPTION</span></span>
<span data-ttu-id="3757e-106">**-AzureBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="3757e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3757e-107">EXAMPLES</span></span>

## <span data-ttu-id="3757e-108">변수</span><span class="sxs-lookup"><span data-stu-id="3757e-108">PARAMETERS</span></span>

### <span data-ttu-id="3757e-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3757e-109">-BatchContext</span></span>
<span data-ttu-id="3757e-110">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3757e-111">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3757e-112">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3757e-113">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3757e-114">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3757e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3757e-115">-DefaultProfile</span></span>
<span data-ttu-id="3757e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3757e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3757e-117">-Force</span></span>
<span data-ttu-id="3757e-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3757e-119">-Id</span><span class="sxs-lookup"><span data-stu-id="3757e-119">-Id</span></span>
<span data-ttu-id="3757e-120">제거할 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3757e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="3757e-121">-Confirm</span></span>
<span data-ttu-id="3757e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3757e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3757e-123">-WhatIf</span></span>
<span data-ttu-id="3757e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3757e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3757e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3757e-126">CommonParameters</span></span>
<span data-ttu-id="3757e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3757e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3757e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3757e-129">입력</span><span class="sxs-lookup"><span data-stu-id="3757e-129">INPUTS</span></span>

### <span data-ttu-id="3757e-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3757e-130">BatchAccountContext</span></span>
<span data-ttu-id="3757e-131">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3757e-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="3757e-132">출력</span><span class="sxs-lookup"><span data-stu-id="3757e-132">OUTPUTS</span></span>

## <span data-ttu-id="3757e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="3757e-133">NOTES</span></span>

## <span data-ttu-id="3757e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3757e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3757e-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3757e-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="3757e-136">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="3757e-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="3757e-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3757e-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="3757e-138">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3757e-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="3757e-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3757e-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="3757e-140">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3757e-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


