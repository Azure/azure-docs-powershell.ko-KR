---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: fff89f2b6d37dc75923527fdb07a71d79dee80a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536564"
---
# <span data-ttu-id="29759-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="29759-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="29759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29759-102">SYNOPSIS</span></span>
<span data-ttu-id="29759-103">경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29759-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29759-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29759-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation]
 -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29759-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29759-105">DESCRIPTION</span></span>
<span data-ttu-id="29759-106">**새 AzureRmRouteTable** Cmdlet은 Azure 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29759-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="29759-107">예제의</span><span class="sxs-lookup"><span data-stu-id="29759-107">EXAMPLES</span></span>

### <span data-ttu-id="29759-108">예제 1: 경로를 포함 하는 경로 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="29759-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="29759-109">첫 번째 명령은 New-AzureRmRouteConfig cmdlet을 사용 하 여 Route07 이라는 경로를 만든 다음 $Route 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="29759-110">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="29759-111">두 번째 명령은 RouteTable01 이라는 경로 테이블을 만들고 $Route에 저장 된 경로를 새 테이블에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="29759-112">명령은 테이블이 속한 리소스 그룹과 테이블의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="29759-113">변수</span><span class="sxs-lookup"><span data-stu-id="29759-113">PARAMETERS</span></span>

### <span data-ttu-id="29759-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29759-114">-AsJob</span></span>
<span data-ttu-id="29759-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="29759-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29759-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29759-116">-DefaultProfile</span></span>
<span data-ttu-id="29759-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29759-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29759-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="29759-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="29759-119">BGP 경로 자동 전파를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="29759-120">-Force</span><span class="sxs-lookup"><span data-stu-id="29759-120">-Force</span></span>
<span data-ttu-id="29759-121">이름이 같은 경로 테이블이 이미 있는 경우에도이 cmdlet이 경로 테이블을 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="29759-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="29759-122">-위치</span><span class="sxs-lookup"><span data-stu-id="29759-122">-Location</span></span>
<span data-ttu-id="29759-123">이 cmdlet이 경로 테이블을 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="29759-124">자세한 내용은 [Azure 지역을](https://azure.microsoft.com/en-us/regions/)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29759-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="29759-125">-이름</span><span class="sxs-lookup"><span data-stu-id="29759-125">-Name</span></span>
<span data-ttu-id="29759-126">경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="29759-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29759-127">-ResourceGroupName</span></span>
<span data-ttu-id="29759-128">이 cmdlet이 경로 테이블을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="29759-129">-경로</span><span class="sxs-lookup"><span data-stu-id="29759-129">-Route</span></span>
<span data-ttu-id="29759-130">경로 테이블과 연결할 **route** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29759-131">태그</span><span class="sxs-lookup"><span data-stu-id="29759-131">-Tag</span></span>
<span data-ttu-id="29759-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="29759-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="29759-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="29759-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="29759-134">-확인</span><span class="sxs-lookup"><span data-stu-id="29759-134">-Confirm</span></span>
<span data-ttu-id="29759-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29759-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29759-136">-WhatIf</span></span>
<span data-ttu-id="29759-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29759-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29759-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29759-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29759-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29759-139">CommonParameters</span></span>
<span data-ttu-id="29759-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29759-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29759-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29759-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29759-142">입력</span><span class="sxs-lookup"><span data-stu-id="29759-142">INPUTS</span></span>

### <span data-ttu-id="29759-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="29759-143">System.String</span></span>

### <span data-ttu-id="29759-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="29759-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="29759-145">System.webserver. 목록 \` 1 [[Microsoft azure. 6.4.1.0. 모델-PSRoute, Microsoft azure. commands. 네트워크, 버전 =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="29759-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRoute, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="29759-146">출력</span><span class="sxs-lookup"><span data-stu-id="29759-146">OUTPUTS</span></span>

### <span data-ttu-id="29759-147">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="29759-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="29759-148">상속자</span><span class="sxs-lookup"><span data-stu-id="29759-148">NOTES</span></span>

## <span data-ttu-id="29759-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29759-149">RELATED LINKS</span></span>

[<span data-ttu-id="29759-150">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="29759-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="29759-151">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="29759-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="29759-152">제거-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="29759-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="29759-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="29759-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
