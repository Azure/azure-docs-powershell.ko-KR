---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491392"
---
# <span data-ttu-id="3a388-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a388-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="3a388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a388-102">SYNOPSIS</span></span>
<span data-ttu-id="3a388-103">두 슬롯을 웹앱으로 교환</span><span class="sxs-lookup"><span data-stu-id="3a388-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="3a388-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a388-104">SYNTAX</span></span>

### <span data-ttu-id="3a388-105">S1</span><span class="sxs-lookup"><span data-stu-id="3a388-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a388-106">S2</span><span class="sxs-lookup"><span data-stu-id="3a388-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a388-107">설명</span><span class="sxs-lookup"><span data-stu-id="3a388-107">DESCRIPTION</span></span>
<span data-ttu-id="3a388-108">**Switch-AzWebAppSlot은** Azure 웹앱과 연결된 두 개의 슬롯을 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="3a388-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="3a388-109">예제</span><span class="sxs-lookup"><span data-stu-id="3a388-109">EXAMPLES</span></span>

### <span data-ttu-id="3a388-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a388-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="3a388-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp이 "destinationslot"인 슬롯 "sourceslot" 슬롯을 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="3a388-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3a388-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a388-112">PARAMETERS</span></span>

### <span data-ttu-id="3a388-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a388-113">-DefaultProfile</span></span>
<span data-ttu-id="3a388-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a388-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a388-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="3a388-115">-DestinationSlotName</span></span>
<span data-ttu-id="3a388-116">대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="3a388-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="3a388-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3a388-117">-Name</span></span>
<span data-ttu-id="3a388-118">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="3a388-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="3a388-119">-PreserveVnet</span></span>
<span data-ttu-id="3a388-120">Vnet 부울 유지</span><span class="sxs-lookup"><span data-stu-id="3a388-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a388-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a388-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3a388-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="3a388-123">-SourceSlotName</span></span>
<span data-ttu-id="3a388-124">원본 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="3a388-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="3a388-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="3a388-126">미리 보기 작업으로 교환</span><span class="sxs-lookup"><span data-stu-id="3a388-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3a388-127">-WebApp</span></span>
<span data-ttu-id="3a388-128">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="3a388-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a388-129">-Confirm</span></span>
<span data-ttu-id="3a388-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a388-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a388-131">-WhatIf</span></span>
<span data-ttu-id="3a388-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3a388-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a388-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a388-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a388-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a388-134">CommonParameters</span></span>
<span data-ttu-id="3a388-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a388-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a388-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3a388-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a388-137">입력</span><span class="sxs-lookup"><span data-stu-id="3a388-137">INPUTS</span></span>

### <span data-ttu-id="3a388-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3a388-138">System.String</span></span>

### <span data-ttu-id="3a388-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="3a388-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3a388-140">출력</span><span class="sxs-lookup"><span data-stu-id="3a388-140">OUTPUTS</span></span>

### <span data-ttu-id="3a388-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="3a388-141">System.Void</span></span>

## <span data-ttu-id="3a388-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a388-142">NOTES</span></span>

## <span data-ttu-id="3a388-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a388-143">RELATED LINKS</span></span>
