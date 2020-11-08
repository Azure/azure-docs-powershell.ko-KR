---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216400"
---
# <span data-ttu-id="d3398-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d3398-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="d3398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3398-102">SYNOPSIS</span></span>
<span data-ttu-id="d3398-103">Azure VirtualRouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="d3398-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3398-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3398-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3398-105">DESCRIPTION</span></span>
<span data-ttu-id="d3398-106">**AzVirtualRouter** Cmdlet은 Azure virtualrouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="d3398-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3398-107">EXAMPLES</span></span>

### <span data-ttu-id="d3398-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3398-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="d3398-109">변수</span><span class="sxs-lookup"><span data-stu-id="d3398-109">PARAMETERS</span></span>

### <span data-ttu-id="d3398-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3398-110">-AsJob</span></span>
<span data-ttu-id="d3398-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3398-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3398-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3398-112">-DefaultProfile</span></span>
<span data-ttu-id="d3398-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3398-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d3398-114">-Force</span></span>
<span data-ttu-id="d3398-115">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="d3398-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3398-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="d3398-116">-HostedSubnet</span></span>
<span data-ttu-id="d3398-117">가상 라우터가 호스팅되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="d3398-118">-위치</span><span class="sxs-lookup"><span data-stu-id="d3398-118">-Location</span></span>
<span data-ttu-id="d3398-119">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-119">The location.</span></span>

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

### <span data-ttu-id="d3398-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d3398-120">-Name</span></span>
<span data-ttu-id="d3398-121">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="d3398-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3398-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3398-123">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="d3398-124">태그</span><span class="sxs-lookup"><span data-stu-id="d3398-124">-Tag</span></span>
<span data-ttu-id="d3398-125">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d3398-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d3398-126">-Confirm</span></span>
<span data-ttu-id="d3398-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3398-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3398-128">-WhatIf</span></span>
<span data-ttu-id="d3398-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3398-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3398-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3398-131">CommonParameters</span></span>
<span data-ttu-id="d3398-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3398-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3398-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3398-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3398-134">입력</span><span class="sxs-lookup"><span data-stu-id="d3398-134">INPUTS</span></span>

### <span data-ttu-id="d3398-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3398-135">System.String</span></span>

### <span data-ttu-id="d3398-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d3398-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d3398-137">출력</span><span class="sxs-lookup"><span data-stu-id="d3398-137">OUTPUTS</span></span>

### <span data-ttu-id="d3398-138">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d3398-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="d3398-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d3398-139">NOTES</span></span>

## <span data-ttu-id="d3398-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3398-140">RELATED LINKS</span></span>
