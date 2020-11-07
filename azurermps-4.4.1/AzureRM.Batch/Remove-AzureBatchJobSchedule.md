---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702770"
---
# <span data-ttu-id="3cf83-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3cf83-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="3cf83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf83-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf83-103">일괄 작업 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3cf83-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3cf83-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf83-106">**-AzureBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="3cf83-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3cf83-107">EXAMPLES</span></span>

## <span data-ttu-id="3cf83-108">변수</span><span class="sxs-lookup"><span data-stu-id="3cf83-108">PARAMETERS</span></span>

### <span data-ttu-id="3cf83-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3cf83-109">-BatchContext</span></span>
<span data-ttu-id="3cf83-110">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3cf83-111">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3cf83-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3cf83-112">-Force</span></span>
<span data-ttu-id="3cf83-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3cf83-114">-Id</span><span class="sxs-lookup"><span data-stu-id="3cf83-114">-Id</span></span>
<span data-ttu-id="3cf83-115">제거할 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="3cf83-116">-확인</span><span class="sxs-lookup"><span data-stu-id="3cf83-116">-Confirm</span></span>
<span data-ttu-id="3cf83-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf83-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf83-118">-WhatIf</span></span>
<span data-ttu-id="3cf83-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf83-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf83-121">-DefaultProfile</span></span>
<span data-ttu-id="3cf83-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf83-123">CommonParameters</span></span>
<span data-ttu-id="3cf83-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf83-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf83-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf83-126">입력</span><span class="sxs-lookup"><span data-stu-id="3cf83-126">INPUTS</span></span>

### <span data-ttu-id="3cf83-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3cf83-127">BatchAccountContext</span></span>
<span data-ttu-id="3cf83-128">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf83-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="3cf83-129">출력</span><span class="sxs-lookup"><span data-stu-id="3cf83-129">OUTPUTS</span></span>

## <span data-ttu-id="3cf83-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3cf83-130">NOTES</span></span>

## <span data-ttu-id="3cf83-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cf83-131">RELATED LINKS</span></span>

[<span data-ttu-id="3cf83-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3cf83-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="3cf83-133">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="3cf83-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="3cf83-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3cf83-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="3cf83-135">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3cf83-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="3cf83-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3cf83-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="3cf83-137">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3cf83-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


