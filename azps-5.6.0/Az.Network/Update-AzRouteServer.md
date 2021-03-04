---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 3cb1fe0fb72182e22c4f7653de26f356ecd823ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951616"
---
# <span data-ttu-id="1853d-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="1853d-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="1853d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1853d-102">SYNOPSIS</span></span>
<span data-ttu-id="1853d-103">Azure RouteServer를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="1853d-104">구문</span><span class="sxs-lookup"><span data-stu-id="1853d-104">SYNTAX</span></span>

### <span data-ttu-id="1853d-105">RouteServerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1853d-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1853d-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1853d-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1853d-107">설명</span><span class="sxs-lookup"><span data-stu-id="1853d-107">DESCRIPTION</span></span>
<span data-ttu-id="1853d-108">**Update-AzRouteServer** cmdlet은 분기-분기 트래픽을 Azure RouteServer로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="1853d-109">예제</span><span class="sxs-lookup"><span data-stu-id="1853d-109">EXAMPLES</span></span>

### <span data-ttu-id="1853d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1853d-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="1853d-111">경로 서버에 대한 분기 트래픽에 분기 트래픽을 사용하도록 설정하려면</span><span class="sxs-lookup"><span data-stu-id="1853d-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="1853d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1853d-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="1853d-113">경로 서버에 대한 분기 트래픽에 분기 트래픽을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="1853d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1853d-114">PARAMETERS</span></span>

### <span data-ttu-id="1853d-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="1853d-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="1853d-116">경로 서버에 대한 분기 트래픽을 분기할 수 있도록 플래그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="1853d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1853d-117">-DefaultProfile</span></span>
<span data-ttu-id="1853d-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1853d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1853d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1853d-120">경로 서버의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-120">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1853d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1853d-121">-ResourceId</span></span>
<span data-ttu-id="1853d-122">경로 서버의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-122">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1853d-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="1853d-123">-RouteServerName</span></span>
<span data-ttu-id="1853d-124">경로 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-124">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1853d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="1853d-125">-Confirm</span></span>
<span data-ttu-id="1853d-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1853d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1853d-127">-WhatIf</span></span>
<span data-ttu-id="1853d-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1853d-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1853d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1853d-130">CommonParameters</span></span>
<span data-ttu-id="1853d-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1853d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1853d-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1853d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1853d-133">입력</span><span class="sxs-lookup"><span data-stu-id="1853d-133">INPUTS</span></span>

### <span data-ttu-id="1853d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1853d-134">System.String</span></span>

## <span data-ttu-id="1853d-135">출력</span><span class="sxs-lookup"><span data-stu-id="1853d-135">OUTPUTS</span></span>

### <span data-ttu-id="1853d-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="1853d-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="1853d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1853d-137">NOTES</span></span>

## <span data-ttu-id="1853d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1853d-138">RELATED LINKS</span></span>
