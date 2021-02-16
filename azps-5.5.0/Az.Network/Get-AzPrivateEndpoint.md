---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189721"
---
# <span data-ttu-id="c5a52-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5a52-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="c5a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5a52-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a52-103">개인 엔드포인트를 얻게</span><span class="sxs-lookup"><span data-stu-id="c5a52-103">Get a private endpoint</span></span>

## <span data-ttu-id="c5a52-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5a52-104">SYNTAX</span></span>

### <span data-ttu-id="c5a52-105">NoExpand(기본값)</span><span class="sxs-lookup"><span data-stu-id="c5a52-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5a52-106">확장</span><span class="sxs-lookup"><span data-stu-id="c5a52-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5a52-107">설명</span><span class="sxs-lookup"><span data-stu-id="c5a52-107">DESCRIPTION</span></span>
<span data-ttu-id="c5a52-108">**Get-AzPrivateEndpoint** cmdlet은 하나 이상의 개인 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="c5a52-109">예제</span><span class="sxs-lookup"><span data-stu-id="c5a52-109">EXAMPLES</span></span>

### <span data-ttu-id="c5a52-110">예제 1: 개인 엔드포인트 검색</span><span class="sxs-lookup"><span data-stu-id="c5a52-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="c5a52-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyPrivateEndpoint1이라는 개인 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="c5a52-112">예제 2: ResourceGroup의 모든 개인 엔드포인트 나열</span><span class="sxs-lookup"><span data-stu-id="c5a52-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="c5a52-113">이 명령은 리소스 그룹 TestResourceGroup의 모든 개인 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="c5a52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5a52-114">PARAMETERS</span></span>

### <span data-ttu-id="c5a52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a52-115">-DefaultProfile</span></span>
<span data-ttu-id="c5a52-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5a52-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c5a52-117">-ExpandResource</span></span>
<span data-ttu-id="c5a52-118">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5a52-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5a52-119">-Name</span></span>
<span data-ttu-id="c5a52-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5a52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a52-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5a52-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5a52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a52-123">CommonParameters</span></span>
<span data-ttu-id="c5a52-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5a52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a52-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5a52-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a52-126">입력</span><span class="sxs-lookup"><span data-stu-id="c5a52-126">INPUTS</span></span>

### <span data-ttu-id="c5a52-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c5a52-127">System.String</span></span>

## <span data-ttu-id="c5a52-128">출력</span><span class="sxs-lookup"><span data-stu-id="c5a52-128">OUTPUTS</span></span>

### <span data-ttu-id="c5a52-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c5a52-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c5a52-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5a52-130">NOTES</span></span>

## <span data-ttu-id="c5a52-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5a52-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5a52-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5a52-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="c5a52-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5a52-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)