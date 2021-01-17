---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362678"
---
# <span data-ttu-id="e384f-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e384f-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="e384f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e384f-102">SYNOPSIS</span></span>
<span data-ttu-id="e384f-103">Azure Virtual WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e384f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e384f-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e384f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e384f-105">DESCRIPTION</span></span>
<span data-ttu-id="e384f-106">새 Azure VirtualWAN 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="e384f-107">예제</span><span class="sxs-lookup"><span data-stu-id="e384f-107">EXAMPLES</span></span>

### <span data-ttu-id="e384f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e384f-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="e384f-109">위에서는 "미국 서부" 지역에 리소스 그룹 "testRG"를 만들고, Azure의 해당 리소스 그룹에서 허용되는 분기-분기 트래픽이 있는 Azure Virtual WAN을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="e384f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e384f-110">PARAMETERS</span></span>

### <span data-ttu-id="e384f-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="e384f-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="e384f-112">VirtualWan에 대한 분기-분기 트래픽을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="e384f-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="e384f-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="e384f-114">VirtualWan에 대한 vnet-vnet 트래픽을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="e384f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e384f-115">-AsJob</span></span>
<span data-ttu-id="e384f-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e384f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e384f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e384f-117">-DefaultProfile</span></span>
<span data-ttu-id="e384f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e384f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e384f-119">-Location</span></span>
<span data-ttu-id="e384f-120">VirtualWAN 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e384f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e384f-121">-Name</span></span>
<span data-ttu-id="e384f-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e384f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e384f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e384f-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e384f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e384f-125">-Tag</span></span>
<span data-ttu-id="e384f-126">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e384f-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e384f-127">-VirtualWANType</span></span>
<span data-ttu-id="e384f-128">Virtual Wan의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e384f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e384f-129">-Confirm</span></span>
<span data-ttu-id="e384f-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e384f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e384f-131">-WhatIf</span></span>
<span data-ttu-id="e384f-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e384f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e384f-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e384f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e384f-134">CommonParameters</span></span>
<span data-ttu-id="e384f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e384f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e384f-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e384f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e384f-137">입력</span><span class="sxs-lookup"><span data-stu-id="e384f-137">INPUTS</span></span>

### <span data-ttu-id="e384f-138">없음</span><span class="sxs-lookup"><span data-stu-id="e384f-138">None</span></span>

## <span data-ttu-id="e384f-139">출력</span><span class="sxs-lookup"><span data-stu-id="e384f-139">OUTPUTS</span></span>

### <span data-ttu-id="e384f-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e384f-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="e384f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e384f-141">NOTES</span></span>

## <span data-ttu-id="e384f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e384f-142">RELATED LINKS</span></span>

[<span data-ttu-id="e384f-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e384f-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="e384f-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e384f-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="e384f-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e384f-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
