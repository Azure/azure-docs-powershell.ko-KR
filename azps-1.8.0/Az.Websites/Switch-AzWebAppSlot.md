---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 8f180eccd92a912820f8d3306ef735c84c30d3a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698283"
---
# <span data-ttu-id="4ace7-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ace7-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="4ace7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ace7-102">SYNOPSIS</span></span>
<span data-ttu-id="4ace7-103">두 슬롯을 웹 앱으로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4ace7-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="4ace7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ace7-104">SYNTAX</span></span>

### <span data-ttu-id="4ace7-105">S1</span><span class="sxs-lookup"><span data-stu-id="4ace7-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ace7-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="4ace7-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ace7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ace7-107">DESCRIPTION</span></span>
<span data-ttu-id="4ace7-108">**AzWebAppSlot** 는 Azure Web App과 연결 된 두 슬롯을 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ace7-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="4ace7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4ace7-109">EXAMPLES</span></span>

### <span data-ttu-id="4ace7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ace7-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="4ace7-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱에 대 한 "destinationslot" 슬롯과 슬롯 "ContosoWebApp 로트" 슬롯을 전환 합니다. 웹-WestUS</span><span class="sxs-lookup"><span data-stu-id="4ace7-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4ace7-112">변수</span><span class="sxs-lookup"><span data-stu-id="4ace7-112">PARAMETERS</span></span>

### <span data-ttu-id="4ace7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ace7-113">-DefaultProfile</span></span>
<span data-ttu-id="4ace7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ace7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ace7-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="4ace7-115">-DestinationSlotName</span></span>
<span data-ttu-id="4ace7-116">대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4ace7-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="4ace7-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4ace7-117">-Name</span></span>
<span data-ttu-id="4ace7-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="4ace7-118">WebApp Name</span></span>

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

### <span data-ttu-id="4ace7-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="4ace7-119">-PreserveVnet</span></span>
<span data-ttu-id="4ace7-120">Vnet 부울 보존</span><span class="sxs-lookup"><span data-stu-id="4ace7-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="4ace7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ace7-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ace7-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4ace7-122">Resource Group Name</span></span>

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

### <span data-ttu-id="4ace7-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="4ace7-123">-SourceSlotName</span></span>
<span data-ttu-id="4ace7-124">원본 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4ace7-124">Source Slot Name</span></span>

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

### <span data-ttu-id="4ace7-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="4ace7-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="4ace7-126">미리 보기 작업으로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4ace7-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="4ace7-127">-Web app</span><span class="sxs-lookup"><span data-stu-id="4ace7-127">-WebApp</span></span>
<span data-ttu-id="4ace7-128">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="4ace7-128">WebApp Object</span></span>

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

### <span data-ttu-id="4ace7-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4ace7-129">-Confirm</span></span>
<span data-ttu-id="4ace7-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ace7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ace7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ace7-131">-WhatIf</span></span>
<span data-ttu-id="4ace7-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ace7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ace7-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ace7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ace7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ace7-134">CommonParameters</span></span>
<span data-ttu-id="4ace7-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ace7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ace7-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ace7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ace7-137">입력</span><span class="sxs-lookup"><span data-stu-id="4ace7-137">INPUTS</span></span>

### <span data-ttu-id="4ace7-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ace7-138">System.String</span></span>

### <span data-ttu-id="4ace7-139">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="4ace7-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4ace7-140">출력</span><span class="sxs-lookup"><span data-stu-id="4ace7-140">OUTPUTS</span></span>

### <span data-ttu-id="4ace7-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4ace7-141">System.Void</span></span>

## <span data-ttu-id="4ace7-142">상속자</span><span class="sxs-lookup"><span data-stu-id="4ace7-142">NOTES</span></span>

## <span data-ttu-id="4ace7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ace7-143">RELATED LINKS</span></span>