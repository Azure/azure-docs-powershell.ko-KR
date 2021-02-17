---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184620"
---
# <span data-ttu-id="428b0-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="428b0-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="428b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="428b0-102">SYNOPSIS</span></span>
<span data-ttu-id="428b0-103">가상 네트워크 탭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="428b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="428b0-104">SYNTAX</span></span>

### <span data-ttu-id="428b0-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="428b0-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="428b0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="428b0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="428b0-107">설명</span><span class="sxs-lookup"><span data-stu-id="428b0-107">DESCRIPTION</span></span>
<span data-ttu-id="428b0-108">**Get-AzVirtualNetworkTap** cmdlet은 Azure 가상 네트워크 탭 또는 리소스 그룹의 Azure 가상 네트워크 탭 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="428b0-109">예제</span><span class="sxs-lookup"><span data-stu-id="428b0-109">EXAMPLES</span></span>

### <span data-ttu-id="428b0-110">예제 1: 가상 네트워크 탭</span><span class="sxs-lookup"><span data-stu-id="428b0-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="428b0-111">이 명령은 "ResourceGroup1"에서 주어진 "VirtualTap1"에 대한 VirtualNetwork 탭 참조를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="428b0-112">예제 2: 필터링을 사용하여 모든 가상 네트워크 탭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="428b0-113">이 명령은 "VirtualTap"로 시작하는 모든 VirtualNetwork 탭 참조를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="428b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="428b0-114">PARAMETERS</span></span>

### <span data-ttu-id="428b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428b0-115">-DefaultProfile</span></span>
<span data-ttu-id="428b0-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428b0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="428b0-117">-Name</span></span>
<span data-ttu-id="428b0-118">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="428b0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428b0-119">-ResourceGroupName</span></span>
<span data-ttu-id="428b0-120">가상 네트워크 탭의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="428b0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="428b0-121">-ResourceId</span></span>
<span data-ttu-id="428b0-122">VirtualNetworkTap 리소스의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="428b0-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428b0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="428b0-123">-Confirm</span></span>
<span data-ttu-id="428b0-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="428b0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="428b0-125">-WhatIf</span></span>
<span data-ttu-id="428b0-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="428b0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="428b0-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="428b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428b0-128">CommonParameters</span></span>
<span data-ttu-id="428b0-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="428b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428b0-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="428b0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428b0-131">입력</span><span class="sxs-lookup"><span data-stu-id="428b0-131">INPUTS</span></span>

### <span data-ttu-id="428b0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="428b0-132">System.String</span></span>

## <span data-ttu-id="428b0-133">출력</span><span class="sxs-lookup"><span data-stu-id="428b0-133">OUTPUTS</span></span>

### <span data-ttu-id="428b0-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="428b0-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="428b0-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="428b0-135">NOTES</span></span>

## <span data-ttu-id="428b0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="428b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="428b0-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="428b0-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="428b0-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="428b0-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="428b0-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="428b0-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
