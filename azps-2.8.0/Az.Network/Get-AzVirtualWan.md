---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: 107f2b7b41143c2f121b358eaf29c99537f51a69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870582"
---
# <span data-ttu-id="28323-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28323-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="28323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28323-102">SYNOPSIS</span></span>
<span data-ttu-id="28323-103">리소스 그룹 또는 구독에서 가상 WAN 또는 모든 가상 Wan을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28323-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="28323-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28323-104">SYNTAX</span></span>

### <span data-ttu-id="28323-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="28323-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28323-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28323-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28323-107">설명은</span><span class="sxs-lookup"><span data-stu-id="28323-107">DESCRIPTION</span></span>
<span data-ttu-id="28323-108">리소스 그룹 또는 구독에서 가상 WAN 또는 모든 가상 Wan을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28323-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="28323-109">예제의</span><span class="sxs-lookup"><span data-stu-id="28323-109">EXAMPLES</span></span>

### <span data-ttu-id="28323-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="28323-110">Example 1</span></span>

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

<span data-ttu-id="28323-111">이 명령은 리소스 그룹 testRG에서 myVirtualWAN 이라는 가상 WAN을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28323-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="28323-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="28323-112">Example 2</span></span>

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

<span data-ttu-id="28323-113">이 명령은 "test"로 시작 하는 모든 가상 Wan을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28323-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="28323-114">변수</span><span class="sxs-lookup"><span data-stu-id="28323-114">PARAMETERS</span></span>

### <span data-ttu-id="28323-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28323-115">-DefaultProfile</span></span>
<span data-ttu-id="28323-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28323-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28323-117">-이름</span><span class="sxs-lookup"><span data-stu-id="28323-117">-Name</span></span>
<span data-ttu-id="28323-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28323-118">The resource name.</span></span>

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

### <span data-ttu-id="28323-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28323-119">-ResourceGroupName</span></span>
<span data-ttu-id="28323-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28323-120">The resource group name.</span></span>

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

### <span data-ttu-id="28323-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28323-121">CommonParameters</span></span>
<span data-ttu-id="28323-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28323-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28323-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28323-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28323-124">입력</span><span class="sxs-lookup"><span data-stu-id="28323-124">INPUTS</span></span>

### <span data-ttu-id="28323-125">않아야</span><span class="sxs-lookup"><span data-stu-id="28323-125">None</span></span>

## <span data-ttu-id="28323-126">출력</span><span class="sxs-lookup"><span data-stu-id="28323-126">OUTPUTS</span></span>

### <span data-ttu-id="28323-127">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28323-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="28323-128">상속자</span><span class="sxs-lookup"><span data-stu-id="28323-128">NOTES</span></span>

## <span data-ttu-id="28323-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28323-129">RELATED LINKS</span></span>

[<span data-ttu-id="28323-130">새로운 AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28323-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="28323-131">제거-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28323-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="28323-132">업데이트-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28323-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
