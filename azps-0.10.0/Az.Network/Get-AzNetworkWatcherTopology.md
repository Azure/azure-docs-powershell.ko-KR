---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 72f5c803c7fa4f4693da3660c41f73eadb464ab7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875541"
---
# <span data-ttu-id="31efc-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="31efc-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="31efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31efc-102">SYNOPSIS</span></span>
<span data-ttu-id="31efc-103">리소스 그룹에 있는 리소스 및 해당 관계의 네트워크 수준 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="31efc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31efc-104">SYNTAX</span></span>

### <span data-ttu-id="31efc-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="31efc-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31efc-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="31efc-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31efc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="31efc-107">DESCRIPTION</span></span>
<span data-ttu-id="31efc-108">Get-AzNetworkWatcherTopology cmdlet은 리소스 그룹의 리소스 및 자원의 관계에 대 한 네트워크 수준 보기를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-108">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="31efc-109">참고: 여러 영역의 리소스가 리소스 그룹에 있는 경우 네트워크 감시자와 동일한 지역에 있는 리소스만 JSON 출력에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="31efc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="31efc-110">EXAMPLES</span></span>

### <span data-ttu-id="31efc-111">--------------------------예제 1: Azure 토폴로지 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="31efc-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="31efc-112">이 예제에서는 VM, Nic, NSG 및 공용 IP가 포함 된 리소스 그룹에서 Get-AzNetworkWatcherTopology cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-112">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="31efc-113">변수</span><span class="sxs-lookup"><span data-stu-id="31efc-113">PARAMETERS</span></span>

### <span data-ttu-id="31efc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31efc-114">-DefaultProfile</span></span>
<span data-ttu-id="31efc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31efc-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31efc-116">-NetworkWatcher</span></span>
<span data-ttu-id="31efc-117">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="31efc-117">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31efc-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="31efc-118">-NetworkWatcherName</span></span>
<span data-ttu-id="31efc-119">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-119">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31efc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31efc-120">-ResourceGroupName</span></span>
<span data-ttu-id="31efc-121">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-121">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31efc-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31efc-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="31efc-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-123">The resource group name.</span></span>

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

### <span data-ttu-id="31efc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31efc-124">CommonParameters</span></span>
<span data-ttu-id="31efc-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31efc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31efc-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31efc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31efc-127">입력</span><span class="sxs-lookup"><span data-stu-id="31efc-127">INPUTS</span></span>

### <span data-ttu-id="31efc-128">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31efc-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="31efc-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31efc-129">System.String</span></span>

## <span data-ttu-id="31efc-130">출력</span><span class="sxs-lookup"><span data-stu-id="31efc-130">OUTPUTS</span></span>

### <span data-ttu-id="31efc-131">PSTopology에 대 한.</span><span class="sxs-lookup"><span data-stu-id="31efc-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="31efc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="31efc-132">NOTES</span></span>
<span data-ttu-id="31efc-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 토폴로지, 보기</span><span class="sxs-lookup"><span data-stu-id="31efc-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="31efc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31efc-134">RELATED LINKS</span></span>

[<span data-ttu-id="31efc-135">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31efc-135">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="31efc-136">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31efc-136">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="31efc-137">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31efc-137">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="31efc-138">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31efc-138">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31efc-139">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="31efc-139">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="31efc-140">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31efc-140">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31efc-141">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31efc-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31efc-142">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31efc-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31efc-143">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="31efc-143">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="31efc-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="31efc-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="31efc-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="31efc-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="31efc-146">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="31efc-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

