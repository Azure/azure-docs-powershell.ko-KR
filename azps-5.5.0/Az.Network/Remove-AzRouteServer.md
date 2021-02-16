---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 2b50d49c108408e1639b5f5f490c2aaafc7bbd82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191721"
---
# <span data-ttu-id="16589-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="16589-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="16589-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16589-102">SYNOPSIS</span></span>
<span data-ttu-id="16589-103">Azure RouteServer를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="16589-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="16589-104">구문</span><span class="sxs-lookup"><span data-stu-id="16589-104">SYNTAX</span></span>

### <span data-ttu-id="16589-105">RouteServerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="16589-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16589-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16589-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16589-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16589-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16589-108">설명</span><span class="sxs-lookup"><span data-stu-id="16589-108">DESCRIPTION</span></span>
<span data-ttu-id="16589-109">**Remove-AzRouteServer** cmdlet은 Azure RouteServer를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="16589-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="16589-110">예제</span><span class="sxs-lookup"><span data-stu-id="16589-110">EXAMPLES</span></span>

### <span data-ttu-id="16589-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="16589-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="16589-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="16589-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="16589-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="16589-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="16589-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16589-114">PARAMETERS</span></span>

### <span data-ttu-id="16589-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16589-115">-AsJob</span></span>
<span data-ttu-id="16589-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="16589-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16589-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16589-117">-DefaultProfile</span></span>
<span data-ttu-id="16589-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16589-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16589-119">-Force</span><span class="sxs-lookup"><span data-stu-id="16589-119">-Force</span></span>
<span data-ttu-id="16589-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16589-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="16589-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16589-121">-InputObject</span></span>
<span data-ttu-id="16589-122">경로 서버 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="16589-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16589-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16589-123">-PassThru</span></span>
<span data-ttu-id="16589-124">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="16589-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="16589-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16589-125">-ResourceGroupName</span></span>
<span data-ttu-id="16589-126">경로 서버의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16589-126">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="16589-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16589-127">-ResourceId</span></span>
<span data-ttu-id="16589-128">경로 서버 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16589-128">The route server resource Id.</span></span>

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

### <span data-ttu-id="16589-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="16589-129">-RouteServerName</span></span>
<span data-ttu-id="16589-130">경로 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16589-130">The name of the route server.</span></span>

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

### <span data-ttu-id="16589-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16589-131">-Confirm</span></span>
<span data-ttu-id="16589-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16589-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16589-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16589-133">-WhatIf</span></span>
<span data-ttu-id="16589-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="16589-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16589-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16589-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16589-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16589-136">CommonParameters</span></span>
<span data-ttu-id="16589-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16589-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16589-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16589-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16589-139">입력</span><span class="sxs-lookup"><span data-stu-id="16589-139">INPUTS</span></span>

### <span data-ttu-id="16589-140">System.String</span><span class="sxs-lookup"><span data-stu-id="16589-140">System.String</span></span>

### <span data-ttu-id="16589-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="16589-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="16589-142">출력</span><span class="sxs-lookup"><span data-stu-id="16589-142">OUTPUTS</span></span>

### <span data-ttu-id="16589-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16589-143">System.Boolean</span></span>

## <span data-ttu-id="16589-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16589-144">NOTES</span></span>

## <span data-ttu-id="16589-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16589-145">RELATED LINKS</span></span>
