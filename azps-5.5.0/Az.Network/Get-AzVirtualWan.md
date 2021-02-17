---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184580"
---
# <span data-ttu-id="f9006-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9006-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="f9006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9006-102">SYNOPSIS</span></span>
<span data-ttu-id="f9006-103">리소스 그룹 또는 구독에서 Virtual WAN 또는 모든 가상 WAN을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="f9006-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9006-104">SYNTAX</span></span>

### <span data-ttu-id="f9006-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9006-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9006-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9006-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9006-107">설명</span><span class="sxs-lookup"><span data-stu-id="f9006-107">DESCRIPTION</span></span>
<span data-ttu-id="f9006-108">리소스 그룹 또는 구독에서 Virtual WAN 또는 모든 가상 WAN을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="f9006-109">예제</span><span class="sxs-lookup"><span data-stu-id="f9006-109">EXAMPLES</span></span>

### <span data-ttu-id="f9006-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9006-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="f9006-111">이 명령은 리소스 그룹 testRG에서 myVirtualWAN이라는 Virtual WAN을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="f9006-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f9006-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="f9006-113">이 명령은 "test"로 시작하는 모든 가상 WA을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="f9006-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9006-114">PARAMETERS</span></span>

### <span data-ttu-id="f9006-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9006-115">-DefaultProfile</span></span>
<span data-ttu-id="f9006-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9006-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f9006-117">-Name</span></span>
<span data-ttu-id="f9006-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f9006-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9006-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9006-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f9006-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9006-121">CommonParameters</span></span>
<span data-ttu-id="f9006-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9006-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9006-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9006-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9006-124">입력</span><span class="sxs-lookup"><span data-stu-id="f9006-124">INPUTS</span></span>

### <span data-ttu-id="f9006-125">없음</span><span class="sxs-lookup"><span data-stu-id="f9006-125">None</span></span>

## <span data-ttu-id="f9006-126">출력</span><span class="sxs-lookup"><span data-stu-id="f9006-126">OUTPUTS</span></span>

### <span data-ttu-id="f9006-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9006-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="f9006-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9006-128">NOTES</span></span>

## <span data-ttu-id="f9006-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9006-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9006-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9006-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="f9006-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9006-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="f9006-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f9006-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
