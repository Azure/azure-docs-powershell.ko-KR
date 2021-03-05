---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: c8959d281c5eda7e2dd3f40941f5c727a000c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982395"
---
# <span data-ttu-id="fd5ae-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fd5ae-101">New-AzIpGroup</span></span>

## <span data-ttu-id="fd5ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5ae-103">Azure IpGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="fd5ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd5ae-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd5ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="fd5ae-106">**New-AzIpGroup** cmdlet은 Azure IpGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="fd5ae-107">예제</span><span class="sxs-lookup"><span data-stu-id="fd5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="fd5ae-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd5ae-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="fd5ae-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="fd5ae-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="fd5ae-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fd5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="fd5ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd5ae-111">-AsJob</span></span>
<span data-ttu-id="fd5ae-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fd5ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd5ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5ae-113">-DefaultProfile</span></span>
<span data-ttu-id="fd5ae-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd5ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd5ae-115">-Force</span></span>
<span data-ttu-id="fd5ae-116">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd5ae-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="fd5ae-117">-IpAddress</span></span>
<span data-ttu-id="fd5ae-118">IpGroup에 정의된 IpAddresses</span><span class="sxs-lookup"><span data-stu-id="fd5ae-118">IpAddresses defined in the IpGroup</span></span>

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

### <span data-ttu-id="fd5ae-119">-Location</span><span class="sxs-lookup"><span data-stu-id="fd5ae-119">-Location</span></span>
<span data-ttu-id="fd5ae-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-120">The location.</span></span>

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

### <span data-ttu-id="fd5ae-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fd5ae-121">-Name</span></span>
<span data-ttu-id="fd5ae-122">ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="fd5ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd5ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd5ae-124">ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="fd5ae-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd5ae-125">-Tag</span></span>
<span data-ttu-id="fd5ae-126">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fd5ae-127">-확인</span><span class="sxs-lookup"><span data-stu-id="fd5ae-127">-Confirm</span></span>
<span data-ttu-id="fd5ae-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd5ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd5ae-129">-WhatIf</span></span>
<span data-ttu-id="fd5ae-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd5ae-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd5ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5ae-132">CommonParameters</span></span>
<span data-ttu-id="fd5ae-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5ae-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd5ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5ae-135">입력</span><span class="sxs-lookup"><span data-stu-id="fd5ae-135">INPUTS</span></span>

### <span data-ttu-id="fd5ae-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fd5ae-136">System.String</span></span>

### <span data-ttu-id="fd5ae-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd5ae-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fd5ae-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd5ae-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd5ae-139">출력</span><span class="sxs-lookup"><span data-stu-id="fd5ae-139">OUTPUTS</span></span>

### <span data-ttu-id="fd5ae-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="fd5ae-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="fd5ae-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd5ae-141">NOTES</span></span>

## <span data-ttu-id="fd5ae-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd5ae-142">RELATED LINKS</span></span>
