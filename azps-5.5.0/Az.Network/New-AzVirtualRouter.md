---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202676"
---
# <span data-ttu-id="e3748-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e3748-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="e3748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3748-102">SYNOPSIS</span></span>
<span data-ttu-id="e3748-103">Azure VirtualRouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="e3748-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3748-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3748-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3748-105">DESCRIPTION</span></span>
<span data-ttu-id="e3748-106">**New-AzVirtualRouter** cmdlet은 Azure VirtualRouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="e3748-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3748-107">EXAMPLES</span></span>

### <span data-ttu-id="e3748-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3748-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="e3748-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3748-109">PARAMETERS</span></span>

### <span data-ttu-id="e3748-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3748-110">-AsJob</span></span>
<span data-ttu-id="e3748-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3748-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3748-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3748-112">-DefaultProfile</span></span>
<span data-ttu-id="e3748-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3748-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e3748-114">-Force</span></span>
<span data-ttu-id="e3748-115">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3748-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="e3748-116">-HostedSubnet</span></span>
<span data-ttu-id="e3748-117">가상 라우터가 호스트되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="e3748-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e3748-118">-Location</span></span>
<span data-ttu-id="e3748-119">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-119">The location.</span></span>

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

### <span data-ttu-id="e3748-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e3748-120">-Name</span></span>
<span data-ttu-id="e3748-121">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="e3748-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3748-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3748-123">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="e3748-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3748-124">-Tag</span></span>
<span data-ttu-id="e3748-125">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e3748-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3748-126">-Confirm</span></span>
<span data-ttu-id="e3748-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3748-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3748-128">-WhatIf</span></span>
<span data-ttu-id="e3748-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3748-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3748-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3748-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3748-131">CommonParameters</span></span>
<span data-ttu-id="e3748-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3748-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3748-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3748-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3748-134">입력</span><span class="sxs-lookup"><span data-stu-id="e3748-134">INPUTS</span></span>

### <span data-ttu-id="e3748-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e3748-135">System.String</span></span>

### <span data-ttu-id="e3748-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3748-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3748-137">출력</span><span class="sxs-lookup"><span data-stu-id="e3748-137">OUTPUTS</span></span>

### <span data-ttu-id="e3748-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e3748-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e3748-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3748-139">NOTES</span></span>

## <span data-ttu-id="e3748-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3748-140">RELATED LINKS</span></span>
