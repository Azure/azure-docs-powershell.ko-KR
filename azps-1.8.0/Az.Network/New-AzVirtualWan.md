---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700252"
---
# <span data-ttu-id="04aff-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="04aff-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="04aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04aff-102">SYNOPSIS</span></span>
<span data-ttu-id="04aff-103">Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="04aff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04aff-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04aff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04aff-105">DESCRIPTION</span></span>
<span data-ttu-id="04aff-106">새 Azure VirtualWAN 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="04aff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04aff-107">EXAMPLES</span></span>

### <span data-ttu-id="04aff-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="04aff-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="04aff-109">위의 작업을 통해 "서쪽 US" 영역에 리소스 그룹 "testRG"을 만들고 Azure에서 해당 리소스 그룹에 허용 되는 분기 트래픽을 분기할 수 있는 Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="04aff-110">변수</span><span class="sxs-lookup"><span data-stu-id="04aff-110">PARAMETERS</span></span>

### <span data-ttu-id="04aff-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="04aff-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="04aff-112">VirtualWan에 대 한 분기 트래픽을 분기할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="04aff-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="04aff-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="04aff-114">VirtualWan에 대 한 vnet에서 vnet로의 트래픽을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="04aff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04aff-115">-AsJob</span></span>
<span data-ttu-id="04aff-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="04aff-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04aff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04aff-117">-DefaultProfile</span></span>
<span data-ttu-id="04aff-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04aff-119">-위치</span><span class="sxs-lookup"><span data-stu-id="04aff-119">-Location</span></span>
<span data-ttu-id="04aff-120">VirtualWAN 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="04aff-121">-이름</span><span class="sxs-lookup"><span data-stu-id="04aff-121">-Name</span></span>
<span data-ttu-id="04aff-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-122">The resource name.</span></span>

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

### <span data-ttu-id="04aff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04aff-123">-ResourceGroupName</span></span>
<span data-ttu-id="04aff-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-124">The resource group name.</span></span>

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

### <span data-ttu-id="04aff-125">태그</span><span class="sxs-lookup"><span data-stu-id="04aff-125">-Tag</span></span>
<span data-ttu-id="04aff-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="04aff-127">-확인</span><span class="sxs-lookup"><span data-stu-id="04aff-127">-Confirm</span></span>
<span data-ttu-id="04aff-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04aff-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04aff-129">-WhatIf</span></span>
<span data-ttu-id="04aff-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04aff-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04aff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04aff-132">CommonParameters</span></span>
<span data-ttu-id="04aff-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04aff-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04aff-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04aff-135">입력</span><span class="sxs-lookup"><span data-stu-id="04aff-135">INPUTS</span></span>

### <span data-ttu-id="04aff-136">않아야</span><span class="sxs-lookup"><span data-stu-id="04aff-136">None</span></span>

## <span data-ttu-id="04aff-137">출력</span><span class="sxs-lookup"><span data-stu-id="04aff-137">OUTPUTS</span></span>

### <span data-ttu-id="04aff-138">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="04aff-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="04aff-139">상속자</span><span class="sxs-lookup"><span data-stu-id="04aff-139">NOTES</span></span>

## <span data-ttu-id="04aff-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04aff-140">RELATED LINKS</span></span>

[<span data-ttu-id="04aff-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="04aff-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="04aff-142">제거-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="04aff-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="04aff-143">업데이트-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="04aff-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
