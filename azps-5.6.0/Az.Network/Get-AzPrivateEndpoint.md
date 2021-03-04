---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 09bd7f919b953c4df09293a75c2c893df4a01b96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954224"
---
# <span data-ttu-id="2521a-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2521a-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="2521a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2521a-102">SYNOPSIS</span></span>
<span data-ttu-id="2521a-103">개인 엔드포인트를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-103">Get a private endpoint</span></span>

## <span data-ttu-id="2521a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2521a-104">SYNTAX</span></span>

### <span data-ttu-id="2521a-105">NoExpand(기본값)</span><span class="sxs-lookup"><span data-stu-id="2521a-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2521a-106">확장</span><span class="sxs-lookup"><span data-stu-id="2521a-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2521a-107">설명</span><span class="sxs-lookup"><span data-stu-id="2521a-107">DESCRIPTION</span></span>
<span data-ttu-id="2521a-108">**Get-AzPrivateEndpoint** cmdlet은 하나 이상의 개인 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="2521a-109">예제</span><span class="sxs-lookup"><span data-stu-id="2521a-109">EXAMPLES</span></span>

### <span data-ttu-id="2521a-110">예제 1: 개인 엔드포인트 검색</span><span class="sxs-lookup"><span data-stu-id="2521a-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="2521a-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyPrivateEndpoint1이라는 개인 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="2521a-112">예제 2: ResourceGroup의 모든 개인 엔드포인트 나열</span><span class="sxs-lookup"><span data-stu-id="2521a-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="2521a-113">이 명령은 리소스 그룹 TestResourceGroup에서 모든 개인 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="2521a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2521a-114">PARAMETERS</span></span>

### <span data-ttu-id="2521a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2521a-115">-DefaultProfile</span></span>
<span data-ttu-id="2521a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2521a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2521a-117">-ExpandResource</span></span>
<span data-ttu-id="2521a-118">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="2521a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2521a-119">-Name</span></span>
<span data-ttu-id="2521a-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-120">The resource name.</span></span>

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

### <span data-ttu-id="2521a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2521a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2521a-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-122">The resource group name.</span></span>

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

### <span data-ttu-id="2521a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2521a-123">CommonParameters</span></span>
<span data-ttu-id="2521a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2521a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2521a-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2521a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2521a-126">입력</span><span class="sxs-lookup"><span data-stu-id="2521a-126">INPUTS</span></span>

### <span data-ttu-id="2521a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2521a-127">System.String</span></span>

## <span data-ttu-id="2521a-128">출력</span><span class="sxs-lookup"><span data-stu-id="2521a-128">OUTPUTS</span></span>

### <span data-ttu-id="2521a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2521a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2521a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2521a-130">NOTES</span></span>

## <span data-ttu-id="2521a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2521a-131">RELATED LINKS</span></span>

[<span data-ttu-id="2521a-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2521a-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="2521a-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2521a-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)