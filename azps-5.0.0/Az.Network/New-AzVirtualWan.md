---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309182"
---
# <span data-ttu-id="6111e-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6111e-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="6111e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6111e-102">SYNOPSIS</span></span>
<span data-ttu-id="6111e-103">Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="6111e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6111e-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6111e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6111e-105">DESCRIPTION</span></span>
<span data-ttu-id="6111e-106">새 Azure VirtualWAN 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="6111e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6111e-107">EXAMPLES</span></span>

### <span data-ttu-id="6111e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6111e-108">Example 1</span></span>

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

<span data-ttu-id="6111e-109">위의 작업을 통해 "서쪽 US" 영역에 리소스 그룹 "testRG"을 만들고 Azure에서 해당 리소스 그룹에 허용 되는 분기 트래픽을 분기할 수 있는 Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="6111e-110">변수</span><span class="sxs-lookup"><span data-stu-id="6111e-110">PARAMETERS</span></span>

### <span data-ttu-id="6111e-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="6111e-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="6111e-112">VirtualWan에 대 한 분기 트래픽을 분기할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="6111e-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="6111e-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="6111e-114">VirtualWan에 대 한 vnet에서 vnet로의 트래픽을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="6111e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6111e-115">-AsJob</span></span>
<span data-ttu-id="6111e-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6111e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6111e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6111e-117">-DefaultProfile</span></span>
<span data-ttu-id="6111e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6111e-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6111e-119">-Location</span></span>
<span data-ttu-id="6111e-120">VirtualWAN 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="6111e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6111e-121">-Name</span></span>
<span data-ttu-id="6111e-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-122">The resource name.</span></span>

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

### <span data-ttu-id="6111e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6111e-123">-ResourceGroupName</span></span>
<span data-ttu-id="6111e-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-124">The resource group name.</span></span>

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

### <span data-ttu-id="6111e-125">태그</span><span class="sxs-lookup"><span data-stu-id="6111e-125">-Tag</span></span>
<span data-ttu-id="6111e-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6111e-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6111e-127">-VirtualWANType</span></span>
<span data-ttu-id="6111e-128">가상 Wan의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="6111e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6111e-129">-Confirm</span></span>
<span data-ttu-id="6111e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6111e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6111e-131">-WhatIf</span></span>
<span data-ttu-id="6111e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6111e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6111e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6111e-134">CommonParameters</span></span>
<span data-ttu-id="6111e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6111e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6111e-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6111e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6111e-137">입력</span><span class="sxs-lookup"><span data-stu-id="6111e-137">INPUTS</span></span>

### <span data-ttu-id="6111e-138">않아야</span><span class="sxs-lookup"><span data-stu-id="6111e-138">None</span></span>

## <span data-ttu-id="6111e-139">출력</span><span class="sxs-lookup"><span data-stu-id="6111e-139">OUTPUTS</span></span>

### <span data-ttu-id="6111e-140">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6111e-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="6111e-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6111e-141">NOTES</span></span>

## <span data-ttu-id="6111e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6111e-142">RELATED LINKS</span></span>

[<span data-ttu-id="6111e-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6111e-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="6111e-144">제거-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6111e-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="6111e-145">업데이트-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6111e-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
