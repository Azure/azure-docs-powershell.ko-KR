---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490967"
---
# <span data-ttu-id="02956-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="02956-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="02956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02956-102">SYNOPSIS</span></span>
<span data-ttu-id="02956-103">경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02956-103">Creates a route filter.</span></span>

## <span data-ttu-id="02956-104">구문</span><span class="sxs-lookup"><span data-stu-id="02956-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02956-105">설명</span><span class="sxs-lookup"><span data-stu-id="02956-105">DESCRIPTION</span></span>
<span data-ttu-id="02956-106">New-AzRouteFilter cmdlet은 Azure 경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02956-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="02956-107">예제</span><span class="sxs-lookup"><span data-stu-id="02956-107">EXAMPLES</span></span>

### <span data-ttu-id="02956-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="02956-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="02956-109">이 명령은 새 경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02956-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="02956-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02956-110">PARAMETERS</span></span>

### <span data-ttu-id="02956-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02956-111">-AsJob</span></span>
<span data-ttu-id="02956-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="02956-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02956-113">-DefaultProfile</span></span>
<span data-ttu-id="02956-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02956-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02956-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02956-115">-Force</span></span>
<span data-ttu-id="02956-116">이름이 같은 경로 필터가 이미 있는 경우에도 이 cmdlet이 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02956-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="02956-117">-Location</span><span class="sxs-lookup"><span data-stu-id="02956-117">-Location</span></span>
<span data-ttu-id="02956-118">이 cmdlet이 경로 필터를 만드는 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02956-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="02956-119">-Name</span><span class="sxs-lookup"><span data-stu-id="02956-119">-Name</span></span>
<span data-ttu-id="02956-120">경로 필터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02956-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="02956-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02956-121">-ResourceGroupName</span></span>
<span data-ttu-id="02956-122">이 cmdlet이 경로 필터를 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02956-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="02956-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="02956-123">-Rule</span></span>
<span data-ttu-id="02956-124">경로 필터와 연결하기 위해 경로 필터 규칙 개체의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02956-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02956-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="02956-125">-Tag</span></span>
<span data-ttu-id="02956-126">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="02956-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="02956-127">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="02956-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="02956-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02956-128">-Confirm</span></span>
<span data-ttu-id="02956-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02956-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02956-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02956-130">-WhatIf</span></span>
<span data-ttu-id="02956-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="02956-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02956-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02956-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02956-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02956-133">CommonParameters</span></span>
<span data-ttu-id="02956-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02956-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02956-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="02956-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02956-136">입력</span><span class="sxs-lookup"><span data-stu-id="02956-136">INPUTS</span></span>

### <span data-ttu-id="02956-137">System.String</span><span class="sxs-lookup"><span data-stu-id="02956-137">System.String</span></span>

### <span data-ttu-id="02956-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="02956-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="02956-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="02956-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02956-140">출력</span><span class="sxs-lookup"><span data-stu-id="02956-140">OUTPUTS</span></span>

### <span data-ttu-id="02956-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="02956-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="02956-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02956-142">NOTES</span></span>
<span data-ttu-id="02956-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="02956-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="02956-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02956-144">RELATED LINKS</span></span>

[<span data-ttu-id="02956-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="02956-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="02956-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="02956-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="02956-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="02956-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="02956-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="02956-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="02956-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="02956-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="02956-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="02956-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="02956-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="02956-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="02956-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="02956-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
