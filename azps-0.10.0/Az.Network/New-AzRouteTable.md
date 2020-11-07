---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: f00840afac4a4d1f0d92316bc859e0a66e7806ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875398"
---
# <span data-ttu-id="43fbe-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fbe-101">New-AzRouteTable</span></span>

## <span data-ttu-id="43fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="43fbe-103">경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-103">Creates a route table.</span></span>

## <span data-ttu-id="43fbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43fbe-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43fbe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="43fbe-105">DESCRIPTION</span></span>
<span data-ttu-id="43fbe-106">**새 AzRouteTable** Cmdlet은 Azure 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="43fbe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="43fbe-107">EXAMPLES</span></span>

### <span data-ttu-id="43fbe-108">예제 1: 경로를 포함 하는 경로 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="43fbe-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="43fbe-109">첫 번째 명령은 New-AzRouteConfig cmdlet을 사용 하 여 Route07 이라는 경로를 만든 다음 $Route 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="43fbe-110">이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="43fbe-111">두 번째 명령은 RouteTable01 이라는 경로 테이블을 만들고 $Route에 저장 된 경로를 새 테이블에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="43fbe-112">명령은 테이블이 속한 리소스 그룹과 테이블의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="43fbe-113">변수</span><span class="sxs-lookup"><span data-stu-id="43fbe-113">PARAMETERS</span></span>

### <span data-ttu-id="43fbe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43fbe-114">-AsJob</span></span>
<span data-ttu-id="43fbe-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="43fbe-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43fbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fbe-116">-DefaultProfile</span></span>
<span data-ttu-id="43fbe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fbe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="43fbe-118">-Force</span></span>
<span data-ttu-id="43fbe-119">이름이 같은 경로 테이블이 이미 있는 경우에도이 cmdlet이 경로 테이블을 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="43fbe-120">-위치</span><span class="sxs-lookup"><span data-stu-id="43fbe-120">-Location</span></span>
<span data-ttu-id="43fbe-121">이 cmdlet이 경로 테이블을 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="43fbe-122">자세한 내용은 [Azure 지역을](http://azure.microsoft.com/en-us/regions/)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="43fbe-122">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="43fbe-123">-이름</span><span class="sxs-lookup"><span data-stu-id="43fbe-123">-Name</span></span>
<span data-ttu-id="43fbe-124">경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-124">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="43fbe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43fbe-125">-ResourceGroupName</span></span>
<span data-ttu-id="43fbe-126">이 cmdlet이 경로 테이블을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="43fbe-127">-경로</span><span class="sxs-lookup"><span data-stu-id="43fbe-127">-Route</span></span>
<span data-ttu-id="43fbe-128">경로 테이블과 연결할 **route** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="43fbe-129">태그</span><span class="sxs-lookup"><span data-stu-id="43fbe-129">-Tag</span></span>
<span data-ttu-id="43fbe-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="43fbe-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="43fbe-131">For example:</span></span>

<span data-ttu-id="43fbe-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="43fbe-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="43fbe-133">-확인</span><span class="sxs-lookup"><span data-stu-id="43fbe-133">-Confirm</span></span>
<span data-ttu-id="43fbe-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fbe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43fbe-135">-WhatIf</span></span>
<span data-ttu-id="43fbe-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43fbe-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fbe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fbe-138">CommonParameters</span></span>
<span data-ttu-id="43fbe-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fbe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fbe-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fbe-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fbe-141">입력</span><span class="sxs-lookup"><span data-stu-id="43fbe-141">INPUTS</span></span>

## <span data-ttu-id="43fbe-142">출력</span><span class="sxs-lookup"><span data-stu-id="43fbe-142">OUTPUTS</span></span>

### <span data-ttu-id="43fbe-143">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="43fbe-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="43fbe-144">상속자</span><span class="sxs-lookup"><span data-stu-id="43fbe-144">NOTES</span></span>

## <span data-ttu-id="43fbe-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43fbe-145">RELATED LINKS</span></span>

[<span data-ttu-id="43fbe-146">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fbe-146">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="43fbe-147">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="43fbe-147">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="43fbe-148">제거-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fbe-148">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="43fbe-149">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fbe-149">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
