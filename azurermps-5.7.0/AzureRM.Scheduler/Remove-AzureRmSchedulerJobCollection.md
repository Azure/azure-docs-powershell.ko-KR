---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b4ff486bac10c79a544761c1946fd3e34dce69a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703546"
---
# <span data-ttu-id="fe7fe-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fe7fe-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="fe7fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7fe-103">작업 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe7fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe7fe-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe7fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7fe-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler에서 작업 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="fe7fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe7fe-107">EXAMPLES</span></span>

## <span data-ttu-id="fe7fe-108">변수</span><span class="sxs-lookup"><span data-stu-id="fe7fe-108">PARAMETERS</span></span>

### <span data-ttu-id="fe7fe-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7fe-109">-DefaultProfile</span></span>
<span data-ttu-id="fe7fe-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe7fe-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="fe7fe-111">-JobCollectionName</span></span>
<span data-ttu-id="fe7fe-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7fe-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe7fe-113">-PassThru</span></span>
<span data-ttu-id="fe7fe-114">이 cmdlet이 성공 시 성공 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="fe7fe-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe7fe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe7fe-116">-ResourceGroupName</span></span>
<span data-ttu-id="fe7fe-117">작업 컬렉션의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7fe-118">-확인</span><span class="sxs-lookup"><span data-stu-id="fe7fe-118">-Confirm</span></span>
<span data-ttu-id="fe7fe-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe7fe-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe7fe-120">-WhatIf</span></span>
<span data-ttu-id="fe7fe-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe7fe-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe7fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7fe-123">CommonParameters</span></span>
<span data-ttu-id="fe7fe-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7fe-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7fe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7fe-126">입력</span><span class="sxs-lookup"><span data-stu-id="fe7fe-126">INPUTS</span></span>

### <span data-ttu-id="fe7fe-127">않아야</span><span class="sxs-lookup"><span data-stu-id="fe7fe-127">None</span></span>
<span data-ttu-id="fe7fe-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe7fe-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe7fe-129">출력</span><span class="sxs-lookup"><span data-stu-id="fe7fe-129">OUTPUTS</span></span>

## <span data-ttu-id="fe7fe-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fe7fe-130">NOTES</span></span>

## <span data-ttu-id="fe7fe-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe7fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe7fe-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fe7fe-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fe7fe-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fe7fe-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fe7fe-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fe7fe-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fe7fe-135">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fe7fe-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fe7fe-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fe7fe-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


