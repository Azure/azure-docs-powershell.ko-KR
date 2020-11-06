---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531177"
---
# <span data-ttu-id="2596c-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="2596c-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="2596c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2596c-102">SYNOPSIS</span></span>
<span data-ttu-id="2596c-103">지정 된 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2596c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2596c-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2596c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2596c-105">DESCRIPTION</span></span>
<span data-ttu-id="2596c-106">**제거-AzureBatchPool** cmdlet은 지정 된 Azure 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="2596c-107">*Force* 매개 변수를 사용 하지 않는 경우 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="2596c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2596c-108">EXAMPLES</span></span>

### <span data-ttu-id="2596c-109">예제 1: 풀 ID를 기준으로 일괄 처리 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="2596c-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="2596c-110">이 명령은 ID MyPool를 사용 하 여 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="2596c-111">삭제 작업을 수행 하기 전에 사용자에 게 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="2596c-112">예제 2: 모든 일괄 처리 풀을 강제 삭제</span><span class="sxs-lookup"><span data-stu-id="2596c-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="2596c-113">이 명령은 모든 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="2596c-114">*Force* 매개 변수가 있으므로 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="2596c-115">변수</span><span class="sxs-lookup"><span data-stu-id="2596c-115">PARAMETERS</span></span>

### <span data-ttu-id="2596c-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2596c-116">-BatchContext</span></span>
<span data-ttu-id="2596c-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2596c-118">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2596c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2596c-119">-Force</span></span>
<span data-ttu-id="2596c-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2596c-121">-Id</span><span class="sxs-lookup"><span data-stu-id="2596c-121">-Id</span></span>
<span data-ttu-id="2596c-122">삭제할 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="2596c-123">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-123">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2596c-124">-확인</span><span class="sxs-lookup"><span data-stu-id="2596c-124">-Confirm</span></span>
<span data-ttu-id="2596c-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2596c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2596c-126">-WhatIf</span></span>
<span data-ttu-id="2596c-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2596c-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2596c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2596c-129">-DefaultProfile</span></span>
<span data-ttu-id="2596c-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2596c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2596c-131">CommonParameters</span></span>
<span data-ttu-id="2596c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2596c-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2596c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2596c-134">입력</span><span class="sxs-lookup"><span data-stu-id="2596c-134">INPUTS</span></span>

### <span data-ttu-id="2596c-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2596c-135">BatchAccountContext</span></span>
<span data-ttu-id="2596c-136">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2596c-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="2596c-137">출력</span><span class="sxs-lookup"><span data-stu-id="2596c-137">OUTPUTS</span></span>

## <span data-ttu-id="2596c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2596c-138">NOTES</span></span>

## <span data-ttu-id="2596c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2596c-139">RELATED LINKS</span></span>

[<span data-ttu-id="2596c-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2596c-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2596c-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="2596c-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="2596c-142">새-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="2596c-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="2596c-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2596c-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


