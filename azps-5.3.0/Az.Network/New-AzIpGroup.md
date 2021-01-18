---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493229"
---
# <span data-ttu-id="eb3c1-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="eb3c1-101">New-AzIpGroup</span></span>

## <span data-ttu-id="eb3c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3c1-103">Azure IpGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="eb3c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb3c1-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb3c1-105">설명</span><span class="sxs-lookup"><span data-stu-id="eb3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3c1-106">**New-AzIpGroup** cmdlet은 Azure IpGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="eb3c1-107">예제</span><span class="sxs-lookup"><span data-stu-id="eb3c1-107">EXAMPLES</span></span>

### <span data-ttu-id="eb3c1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="eb3c1-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="eb3c1-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="eb3c1-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="eb3c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb3c1-110">PARAMETERS</span></span>

### <span data-ttu-id="eb3c1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb3c1-111">-AsJob</span></span>
<span data-ttu-id="eb3c1-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eb3c1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb3c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3c1-113">-DefaultProfile</span></span>
<span data-ttu-id="eb3c1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb3c1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eb3c1-115">-Force</span></span>
<span data-ttu-id="eb3c1-116">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eb3c1-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="eb3c1-117">-IpAddress</span></span>
<span data-ttu-id="eb3c1-118">IpGroup에 정의된 IpAddresses</span><span class="sxs-lookup"><span data-stu-id="eb3c1-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="eb3c1-119">-Location</span></span>
<span data-ttu-id="eb3c1-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb3c1-121">-Name</span></span>
<span data-ttu-id="eb3c1-122">ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb3c1-124">ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb3c1-125">-Tag</span></span>
<span data-ttu-id="eb3c1-126">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb3c1-127">-Confirm</span></span>
<span data-ttu-id="eb3c1-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb3c1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb3c1-129">-WhatIf</span></span>
<span data-ttu-id="eb3c1-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eb3c1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb3c1-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb3c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3c1-132">CommonParameters</span></span>
<span data-ttu-id="eb3c1-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3c1-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3c1-135">입력</span><span class="sxs-lookup"><span data-stu-id="eb3c1-135">INPUTS</span></span>

### <span data-ttu-id="eb3c1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eb3c1-136">System.String</span></span>

### <span data-ttu-id="eb3c1-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eb3c1-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="eb3c1-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eb3c1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eb3c1-139">출력</span><span class="sxs-lookup"><span data-stu-id="eb3c1-139">OUTPUTS</span></span>

### <span data-ttu-id="eb3c1-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="eb3c1-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="eb3c1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb3c1-141">NOTES</span></span>

## <span data-ttu-id="eb3c1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb3c1-142">RELATED LINKS</span></span>
