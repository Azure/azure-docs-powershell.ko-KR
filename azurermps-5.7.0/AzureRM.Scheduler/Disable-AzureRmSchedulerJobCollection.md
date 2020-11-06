---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: c754b7e30fdec3a179beefdf48292a781ec083db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529720"
---
# <span data-ttu-id="2a029-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2a029-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="2a029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a029-102">SYNOPSIS</span></span>
<span data-ttu-id="2a029-103">작업 컬렉션을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a029-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a029-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a029-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a029-105">DESCRIPTION</span></span>
<span data-ttu-id="2a029-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler에서 작업 컬렉션을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="2a029-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2a029-107">EXAMPLES</span></span>

## <span data-ttu-id="2a029-108">변수</span><span class="sxs-lookup"><span data-stu-id="2a029-108">PARAMETERS</span></span>

### <span data-ttu-id="2a029-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a029-109">-DefaultProfile</span></span>
<span data-ttu-id="2a029-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a029-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2a029-111">-JobCollectionName</span></span>
<span data-ttu-id="2a029-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="2a029-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a029-113">-PassThru</span></span>
<span data-ttu-id="2a029-114">이 cmdlet이 성공 시 성공 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="2a029-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a029-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a029-116">-ResourceGroupName</span></span>
<span data-ttu-id="2a029-117">작업 컬렉션의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="2a029-118">-확인</span><span class="sxs-lookup"><span data-stu-id="2a029-118">-Confirm</span></span>
<span data-ttu-id="2a029-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a029-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a029-120">-WhatIf</span></span>
<span data-ttu-id="2a029-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a029-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a029-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a029-123">CommonParameters</span></span>
<span data-ttu-id="2a029-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a029-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a029-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a029-126">입력</span><span class="sxs-lookup"><span data-stu-id="2a029-126">INPUTS</span></span>

### <span data-ttu-id="2a029-127">않아야</span><span class="sxs-lookup"><span data-stu-id="2a029-127">None</span></span>
<span data-ttu-id="2a029-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a029-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a029-129">출력</span><span class="sxs-lookup"><span data-stu-id="2a029-129">OUTPUTS</span></span>

## <span data-ttu-id="2a029-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2a029-130">NOTES</span></span>

## <span data-ttu-id="2a029-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a029-131">RELATED LINKS</span></span>

[<span data-ttu-id="2a029-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2a029-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2a029-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2a029-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2a029-134">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2a029-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2a029-135">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2a029-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2a029-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2a029-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


