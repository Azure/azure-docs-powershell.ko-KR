---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: e7e0b58dfd4ac925110c5f666bc7c360cc222983
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371631"
---
# <span data-ttu-id="c1b4b-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1b4b-101">New-AzRouteTable</span></span>

## <span data-ttu-id="c1b4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b4b-103">경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-103">Creates a route table.</span></span>

## <span data-ttu-id="c1b4b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1b4b-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b4b-105">설명</span><span class="sxs-lookup"><span data-stu-id="c1b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b4b-106">**New-AzRouteTable** cmdlet은 Azure 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="c1b4b-107">예제</span><span class="sxs-lookup"><span data-stu-id="c1b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b4b-108">예제 1: 경로가 포함된 경로 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="c1b4b-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="c1b4b-109">첫 번째 명령은 New-AzRouteConfig cmdlet을 사용하여 Route07이라는 경로를 만든 다음 $Route 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="c1b4b-110">이 경로는 패킷을 로컬 가상 네트워크에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="c1b4b-111">두 번째 명령은 RouteTable01이라는 경로 테이블을 만들고 새 테이블에 $Route 경로를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="c1b4b-112">이 명령은 테이블이 속한 리소스 그룹 및 테이블의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="c1b4b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1b4b-113">PARAMETERS</span></span>

### <span data-ttu-id="c1b4b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1b4b-114">-AsJob</span></span>
<span data-ttu-id="c1b4b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c1b4b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1b4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b4b-116">-DefaultProfile</span></span>
<span data-ttu-id="c1b4b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b4b-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="c1b4b-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="c1b4b-119">BGP 경로 자동 전파를 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="c1b4b-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="c1b4b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c1b4b-120">-Force</span></span>
<span data-ttu-id="c1b4b-121">동일한 이름의 경로 테이블이 이미 있는 경우에도 이 cmdlet이 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="c1b4b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="c1b4b-122">-Location</span></span>
<span data-ttu-id="c1b4b-123">이 cmdlet이 경로 테이블을 만드는 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="c1b4b-124">자세한 내용은 [Azure 지역을 참조하세요.](http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="c1b4b-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="c1b4b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1b4b-125">-Name</span></span>
<span data-ttu-id="c1b4b-126">경로 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="c1b4b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b4b-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1b4b-128">이 cmdlet이 경로 테이블을 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="c1b4b-129">-Route</span><span class="sxs-lookup"><span data-stu-id="c1b4b-129">-Route</span></span>
<span data-ttu-id="c1b4b-130">경로 테이블과 연결하기 위해 **경로** 개체의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b4b-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1b4b-131">-Tag</span></span>
<span data-ttu-id="c1b4b-132">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c1b4b-133">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c1b4b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c1b4b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1b4b-134">-Confirm</span></span>
<span data-ttu-id="c1b4b-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b4b-136">-WhatIf</span></span>
<span data-ttu-id="c1b4b-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c1b4b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b4b-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b4b-139">CommonParameters</span></span>
<span data-ttu-id="c1b4b-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b4b-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b4b-142">입력</span><span class="sxs-lookup"><span data-stu-id="c1b4b-142">INPUTS</span></span>

### <span data-ttu-id="c1b4b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c1b4b-143">System.String</span></span>

### <span data-ttu-id="c1b4b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1b4b-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c1b4b-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span><span class="sxs-lookup"><span data-stu-id="c1b4b-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="c1b4b-146">출력</span><span class="sxs-lookup"><span data-stu-id="c1b4b-146">OUTPUTS</span></span>

### <span data-ttu-id="c1b4b-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1b4b-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c1b4b-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1b4b-148">NOTES</span></span>

## <span data-ttu-id="c1b4b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1b4b-149">RELATED LINKS</span></span>

[<span data-ttu-id="c1b4b-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1b4b-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c1b4b-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c1b4b-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="c1b4b-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1b4b-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="c1b4b-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1b4b-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
