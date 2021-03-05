---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 608be77335c0201b8ae1d17b34057025392f1072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978251"
---
# <span data-ttu-id="4aa75-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4aa75-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="4aa75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa75-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa75-103">Azure VirtualRouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="4aa75-104">구문</span><span class="sxs-lookup"><span data-stu-id="4aa75-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4aa75-105">설명</span><span class="sxs-lookup"><span data-stu-id="4aa75-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa75-106">**New-AzVirtualRouter** cmdlet은 Azure VirtualRouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="4aa75-107">예제</span><span class="sxs-lookup"><span data-stu-id="4aa75-107">EXAMPLES</span></span>

### <span data-ttu-id="4aa75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4aa75-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="4aa75-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4aa75-109">PARAMETERS</span></span>

### <span data-ttu-id="4aa75-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aa75-110">-AsJob</span></span>
<span data-ttu-id="4aa75-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4aa75-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4aa75-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa75-112">-DefaultProfile</span></span>
<span data-ttu-id="4aa75-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa75-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4aa75-114">-Force</span></span>
<span data-ttu-id="4aa75-115">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4aa75-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="4aa75-116">-HostedSubnet</span></span>
<span data-ttu-id="4aa75-117">가상 라우터가 호스트되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="4aa75-118">-Location</span><span class="sxs-lookup"><span data-stu-id="4aa75-118">-Location</span></span>
<span data-ttu-id="4aa75-119">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-119">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa75-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4aa75-120">-Name</span></span>
<span data-ttu-id="4aa75-121">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa75-122">-ResourceGroupName</span></span>
<span data-ttu-id="4aa75-123">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-123">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa75-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4aa75-124">-Tag</span></span>
<span data-ttu-id="4aa75-125">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa75-126">-확인</span><span class="sxs-lookup"><span data-stu-id="4aa75-126">-Confirm</span></span>
<span data-ttu-id="4aa75-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa75-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa75-128">-WhatIf</span></span>
<span data-ttu-id="4aa75-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa75-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa75-131">CommonParameters</span></span>
<span data-ttu-id="4aa75-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa75-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aa75-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa75-134">입력</span><span class="sxs-lookup"><span data-stu-id="4aa75-134">INPUTS</span></span>

### <span data-ttu-id="4aa75-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4aa75-135">System.String</span></span>

### <span data-ttu-id="4aa75-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4aa75-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4aa75-137">출력</span><span class="sxs-lookup"><span data-stu-id="4aa75-137">OUTPUTS</span></span>

### <span data-ttu-id="4aa75-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4aa75-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="4aa75-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4aa75-139">NOTES</span></span>

## <span data-ttu-id="4aa75-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aa75-140">RELATED LINKS</span></span>
