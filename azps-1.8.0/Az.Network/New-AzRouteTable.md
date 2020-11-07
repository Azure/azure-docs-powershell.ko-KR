---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700280"
---
# <span data-ttu-id="cce68-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cce68-101">New-AzRouteTable</span></span>

## <span data-ttu-id="cce68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce68-102">SYNOPSIS</span></span>
<span data-ttu-id="cce68-103">경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-103">Creates a route table.</span></span>

## <span data-ttu-id="cce68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cce68-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cce68-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cce68-105">DESCRIPTION</span></span>
<span data-ttu-id="cce68-106">**새 AzRouteTable** Cmdlet은 Azure 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="cce68-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cce68-107">EXAMPLES</span></span>

### <span data-ttu-id="cce68-108">예제 1: 경로를 포함 하는 경로 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="cce68-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="cce68-109">첫 번째 명령은 New-AzRouteConfig cmdlet을 사용 하 여 Route07 이라는 경로를 만든 다음 $Route 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="cce68-110">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="cce68-111">두 번째 명령은 RouteTable01 이라는 경로 테이블을 만들고 $Route에 저장 된 경로를 새 테이블에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="cce68-112">명령은 테이블이 속한 리소스 그룹과 테이블의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="cce68-113">변수</span><span class="sxs-lookup"><span data-stu-id="cce68-113">PARAMETERS</span></span>

### <span data-ttu-id="cce68-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cce68-114">-AsJob</span></span>
<span data-ttu-id="cce68-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cce68-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cce68-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce68-116">-DefaultProfile</span></span>
<span data-ttu-id="cce68-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce68-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="cce68-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="cce68-119">BGP 경로 자동 전파를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="cce68-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cce68-120">-Force</span></span>
<span data-ttu-id="cce68-121">이름이 같은 경로 테이블이 이미 있는 경우에도이 cmdlet이 경로 테이블을 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="cce68-122">-위치</span><span class="sxs-lookup"><span data-stu-id="cce68-122">-Location</span></span>
<span data-ttu-id="cce68-123">이 cmdlet이 경로 테이블을 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="cce68-124">자세한 내용은 [Azure 지역을](https://azure.microsoft.com/en-us/regions/)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cce68-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="cce68-125">-이름</span><span class="sxs-lookup"><span data-stu-id="cce68-125">-Name</span></span>
<span data-ttu-id="cce68-126">경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="cce68-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce68-127">-ResourceGroupName</span></span>
<span data-ttu-id="cce68-128">이 cmdlet이 경로 테이블을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="cce68-129">-경로</span><span class="sxs-lookup"><span data-stu-id="cce68-129">-Route</span></span>
<span data-ttu-id="cce68-130">경로 테이블과 연결할 **route** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="cce68-131">태그</span><span class="sxs-lookup"><span data-stu-id="cce68-131">-Tag</span></span>
<span data-ttu-id="cce68-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cce68-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cce68-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cce68-134">-확인</span><span class="sxs-lookup"><span data-stu-id="cce68-134">-Confirm</span></span>
<span data-ttu-id="cce68-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cce68-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cce68-136">-WhatIf</span></span>
<span data-ttu-id="cce68-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cce68-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cce68-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce68-139">CommonParameters</span></span>
<span data-ttu-id="cce68-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce68-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce68-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce68-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce68-142">입력</span><span class="sxs-lookup"><span data-stu-id="cce68-142">INPUTS</span></span>

### <span data-ttu-id="cce68-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cce68-143">System.String</span></span>

### <span data-ttu-id="cce68-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="cce68-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cce68-145">Microsoft Azure. \* PSRoute []</span><span class="sxs-lookup"><span data-stu-id="cce68-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="cce68-146">출력</span><span class="sxs-lookup"><span data-stu-id="cce68-146">OUTPUTS</span></span>

### <span data-ttu-id="cce68-147">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cce68-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="cce68-148">상속자</span><span class="sxs-lookup"><span data-stu-id="cce68-148">NOTES</span></span>

## <span data-ttu-id="cce68-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cce68-149">RELATED LINKS</span></span>

[<span data-ttu-id="cce68-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cce68-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="cce68-151">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cce68-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="cce68-152">제거-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cce68-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="cce68-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cce68-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
