---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 59f8b74a9815820b1ace1e9d7defeb5b9dd85efa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870642"
---
# <span data-ttu-id="f129b-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f129b-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="f129b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f129b-102">SYNOPSIS</span></span>
<span data-ttu-id="f129b-103">개인 끝점 가져오기</span><span class="sxs-lookup"><span data-stu-id="f129b-103">Get a private endpoint</span></span>

## <span data-ttu-id="f129b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f129b-104">SYNTAX</span></span>

### <span data-ttu-id="f129b-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="f129b-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f129b-106">확장</span><span class="sxs-lookup"><span data-stu-id="f129b-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f129b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f129b-107">DESCRIPTION</span></span>
<span data-ttu-id="f129b-108">**AzPrivateEndpoint** cmdlet은 하나 이상의 비공개 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="f129b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f129b-109">EXAMPLES</span></span>

### <span data-ttu-id="f129b-110">1: 개인 끝점 검색</span><span class="sxs-lookup"><span data-stu-id="f129b-110">1: Retrieve a private endpoint</span></span>
```
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

<span data-ttu-id="f129b-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyPrivateEndpoint1 라는 개인 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="f129b-112">2: ResourceGroup의 모든 개인 끝점 나열</span><span class="sxs-lookup"><span data-stu-id="f129b-112">2: List all private endpoints in ResourceGroup</span></span>
```
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

<span data-ttu-id="f129b-113">이 명령은 리소스 그룹 TestResourceGroup의 모든 비공개 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="f129b-114">변수</span><span class="sxs-lookup"><span data-stu-id="f129b-114">PARAMETERS</span></span>

### <span data-ttu-id="f129b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f129b-115">-DefaultProfile</span></span>
<span data-ttu-id="f129b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f129b-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f129b-117">-ExpandResource</span></span>
<span data-ttu-id="f129b-118">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="f129b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f129b-119">-Name</span></span>
<span data-ttu-id="f129b-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-120">The resource name.</span></span>

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

### <span data-ttu-id="f129b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f129b-121">-ResourceGroupName</span></span>
<span data-ttu-id="f129b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-122">The resource group name.</span></span>

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

### <span data-ttu-id="f129b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f129b-123">CommonParameters</span></span>
<span data-ttu-id="f129b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f129b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f129b-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f129b-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f129b-126">입력</span><span class="sxs-lookup"><span data-stu-id="f129b-126">INPUTS</span></span>

### <span data-ttu-id="f129b-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f129b-127">System.String</span></span>

## <span data-ttu-id="f129b-128">출력</span><span class="sxs-lookup"><span data-stu-id="f129b-128">OUTPUTS</span></span>

### <span data-ttu-id="f129b-129">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f129b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f129b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f129b-130">NOTES</span></span>

## <span data-ttu-id="f129b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f129b-131">RELATED LINKS</span></span>

[<span data-ttu-id="f129b-132">새로운 AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f129b-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="f129b-133">제거-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f129b-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)