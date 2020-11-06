---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: e1cfb3e70ab8176cfd686dc404b13dbbfb23e4e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526468"
---
# <span data-ttu-id="d842c-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d842c-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d842c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d842c-102">SYNOPSIS</span></span>
<span data-ttu-id="d842c-103">두 슬롯을 웹 앱으로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="d842c-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d842c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d842c-104">SYNTAX</span></span>

### <span data-ttu-id="d842c-105">S1</span><span class="sxs-lookup"><span data-stu-id="d842c-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d842c-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="d842c-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d842c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d842c-107">DESCRIPTION</span></span>
<span data-ttu-id="d842c-108">**AzureRmWebAppSlot** 는 Azure Web App과 연결 된 두 슬롯을 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="d842c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d842c-109">EXAMPLES</span></span>

### <span data-ttu-id="d842c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d842c-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d842c-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱에 대 한 "destinationslot" 슬롯과 슬롯 "ContosoWebApp 로트" 슬롯을 전환 합니다. 웹-WestUS</span><span class="sxs-lookup"><span data-stu-id="d842c-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d842c-112">변수</span><span class="sxs-lookup"><span data-stu-id="d842c-112">PARAMETERS</span></span>

### <span data-ttu-id="d842c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d842c-113">-DefaultProfile</span></span>
<span data-ttu-id="d842c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d842c-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="d842c-115">-DestinationSlotName</span></span>
<span data-ttu-id="d842c-116">대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="d842c-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d842c-117">-Name</span></span>
<span data-ttu-id="d842c-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="d842c-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="d842c-119">-PreserveVnet</span></span>
<span data-ttu-id="d842c-120">Vnet 부울 보존</span><span class="sxs-lookup"><span data-stu-id="d842c-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d842c-121">-ResourceGroupName</span></span>
<span data-ttu-id="d842c-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d842c-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="d842c-123">-SourceSlotName</span></span>
<span data-ttu-id="d842c-124">원본 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="d842c-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="d842c-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="d842c-126">미리 보기 작업으로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="d842c-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-127">-Web app</span><span class="sxs-lookup"><span data-stu-id="d842c-127">-WebApp</span></span>
<span data-ttu-id="d842c-128">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="d842c-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d842c-129">-Confirm</span></span>
<span data-ttu-id="d842c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d842c-131">-WhatIf</span></span>
<span data-ttu-id="d842c-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d842c-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d842c-134">CommonParameters</span></span>
<span data-ttu-id="d842c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d842c-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d842c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d842c-137">입력</span><span class="sxs-lookup"><span data-stu-id="d842c-137">INPUTS</span></span>

### <span data-ttu-id="d842c-138">Site</span><span class="sxs-lookup"><span data-stu-id="d842c-138">Site</span></span>
<span data-ttu-id="d842c-139">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d842c-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d842c-140">출력</span><span class="sxs-lookup"><span data-stu-id="d842c-140">OUTPUTS</span></span>

## <span data-ttu-id="d842c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d842c-141">NOTES</span></span>

## <span data-ttu-id="d842c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d842c-142">RELATED LINKS</span></span>

