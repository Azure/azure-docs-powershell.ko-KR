---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 9673c236886feb801d6e4078bfccbf82e2339811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529396"
---
# <span data-ttu-id="14779-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="14779-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="14779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14779-102">SYNOPSIS</span></span>
<span data-ttu-id="14779-103">작업 컬렉션을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14779-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14779-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14779-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14779-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14779-105">DESCRIPTION</span></span>
<span data-ttu-id="14779-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler에서 작업 컬렉션을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14779-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="14779-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14779-107">EXAMPLES</span></span>

## <span data-ttu-id="14779-108">변수</span><span class="sxs-lookup"><span data-stu-id="14779-108">PARAMETERS</span></span>

### <span data-ttu-id="14779-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14779-109">-DefaultProfile</span></span>
<span data-ttu-id="14779-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14779-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14779-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="14779-111">-JobCollectionName</span></span>
<span data-ttu-id="14779-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14779-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14779-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14779-113">-PassThru</span></span>
<span data-ttu-id="14779-114">이 cmdlet이 성공 시 성공 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14779-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="14779-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14779-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14779-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14779-116">-ResourceGroupName</span></span>
<span data-ttu-id="14779-117">작업 컬렉션의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14779-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14779-118">-확인</span><span class="sxs-lookup"><span data-stu-id="14779-118">-Confirm</span></span>
<span data-ttu-id="14779-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14779-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14779-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14779-120">-WhatIf</span></span>
<span data-ttu-id="14779-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14779-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14779-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14779-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14779-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14779-123">CommonParameters</span></span>
<span data-ttu-id="14779-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14779-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14779-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14779-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14779-126">입력</span><span class="sxs-lookup"><span data-stu-id="14779-126">INPUTS</span></span>

### <span data-ttu-id="14779-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14779-127">System.String</span></span>

## <span data-ttu-id="14779-128">출력</span><span class="sxs-lookup"><span data-stu-id="14779-128">OUTPUTS</span></span>

### <span data-ttu-id="14779-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14779-129">System.String</span></span>

## <span data-ttu-id="14779-130">상속자</span><span class="sxs-lookup"><span data-stu-id="14779-130">NOTES</span></span>

## <span data-ttu-id="14779-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14779-131">RELATED LINKS</span></span>

[<span data-ttu-id="14779-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="14779-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="14779-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="14779-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="14779-134">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="14779-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="14779-135">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="14779-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="14779-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="14779-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


