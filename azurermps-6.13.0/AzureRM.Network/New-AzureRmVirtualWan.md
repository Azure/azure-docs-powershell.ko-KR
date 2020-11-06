---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536563"
---
# <span data-ttu-id="09299-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="09299-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="09299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09299-102">SYNOPSIS</span></span>
<span data-ttu-id="09299-103">Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09299-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09299-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09299-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09299-105">설명은</span><span class="sxs-lookup"><span data-stu-id="09299-105">DESCRIPTION</span></span>
<span data-ttu-id="09299-106">새 Azure VirtualWAN 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09299-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="09299-107">예제의</span><span class="sxs-lookup"><span data-stu-id="09299-107">EXAMPLES</span></span>

### <span data-ttu-id="09299-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="09299-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="09299-109">위의 작업을 통해 "서쪽 US" 영역에 리소스 그룹 "testRG"을 만들고 Azure에서 해당 리소스 그룹에 허용 되는 분기 트래픽을 분기할 수 있는 Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09299-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="09299-110">변수</span><span class="sxs-lookup"><span data-stu-id="09299-110">PARAMETERS</span></span>

### <span data-ttu-id="09299-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="09299-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="09299-112">VirtualWan에 대 한 분기 트래픽을 분기할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="09299-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="09299-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="09299-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="09299-114">VirtualWan에 대 한 vnet에서 vnet로의 트래픽을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="09299-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="09299-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09299-115">-AsJob</span></span>
<span data-ttu-id="09299-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="09299-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09299-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09299-117">-DefaultProfile</span></span>
<span data-ttu-id="09299-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09299-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09299-119">-위치</span><span class="sxs-lookup"><span data-stu-id="09299-119">-Location</span></span>
<span data-ttu-id="09299-120">VirtualWAN 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="09299-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09299-121">-이름</span><span class="sxs-lookup"><span data-stu-id="09299-121">-Name</span></span>
<span data-ttu-id="09299-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09299-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09299-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09299-123">-ResourceGroupName</span></span>
<span data-ttu-id="09299-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09299-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09299-125">태그</span><span class="sxs-lookup"><span data-stu-id="09299-125">-Tag</span></span>
<span data-ttu-id="09299-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="09299-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09299-127">-확인</span><span class="sxs-lookup"><span data-stu-id="09299-127">-Confirm</span></span>
<span data-ttu-id="09299-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09299-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09299-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09299-129">-WhatIf</span></span>
<span data-ttu-id="09299-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09299-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09299-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09299-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09299-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09299-132">CommonParameters</span></span>
<span data-ttu-id="09299-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09299-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09299-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09299-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09299-135">입력</span><span class="sxs-lookup"><span data-stu-id="09299-135">INPUTS</span></span>

### <span data-ttu-id="09299-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="09299-136">System.String</span></span>

### <span data-ttu-id="09299-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="09299-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="09299-138">출력</span><span class="sxs-lookup"><span data-stu-id="09299-138">OUTPUTS</span></span>

### <span data-ttu-id="09299-139">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="09299-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="09299-140">상속자</span><span class="sxs-lookup"><span data-stu-id="09299-140">NOTES</span></span>

## <span data-ttu-id="09299-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09299-141">RELATED LINKS</span></span>
