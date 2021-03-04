---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 2838d3d18aaa1cdf450eed184c5ebfe9a803c20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951835"
---
# <span data-ttu-id="5fc5b-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc5b-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="5fc5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc5b-103">Virtual Network Gateway에서 패킷 캡처 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="5fc5b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5fc5b-104">SYNTAX</span></span>

### <span data-ttu-id="5fc5b-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="5fc5b-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc5b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5fc5b-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc5b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc5b-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fc5b-108">설명</span><span class="sxs-lookup"><span data-stu-id="5fc5b-108">DESCRIPTION</span></span>
<span data-ttu-id="5fc5b-109">Virtual Network Gateway에서 패킷 캡처 작업을 중지하고 해당 저장소 컨테이너의 SasUrl에 결과를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="5fc5b-110">예제</span><span class="sxs-lookup"><span data-stu-id="5fc5b-110">EXAMPLES</span></span>

### <span data-ttu-id="5fc5b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5fc5b-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="5fc5b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5fc5b-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="5fc5b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fc5b-113">PARAMETERS</span></span>

### <span data-ttu-id="5fc5b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fc5b-114">-AsJob</span></span>
<span data-ttu-id="5fc5b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5fc5b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fc5b-116">-확인</span><span class="sxs-lookup"><span data-stu-id="5fc5b-116">-Confirm</span></span>
<span data-ttu-id="5fc5b-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc5b-118">-DefaultProfile</span></span>
<span data-ttu-id="5fc5b-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fc5b-120">-InputObject</span></span>
<span data-ttu-id="5fc5b-121">패킷 캡처를 시작할 가상 네트워크 게이트웨이 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-121">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5fc5b-122">-Name</span></span>
<span data-ttu-id="5fc5b-123">패킷 캡처를 시작할 가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-123">The virtual network gateway name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5fc5b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc5b-126">-ResourceId</span></span>
<span data-ttu-id="5fc5b-127">패킷 캡처를 시작할 VirtualNetworkGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="5fc5b-128">-SasUrl</span></span>
<span data-ttu-id="5fc5b-129">가상 네트워크 게이트웨이에서 SAS URL 패킷 캡처.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-129">SAS URL packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fc5b-130">-WhatIf</span></span>
<span data-ttu-id="5fc5b-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fc5b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc5b-133">CommonParameters</span></span>
<span data-ttu-id="5fc5b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc5b-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fc5b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc5b-136">입력</span><span class="sxs-lookup"><span data-stu-id="5fc5b-136">INPUTS</span></span>

### <span data-ttu-id="5fc5b-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5fc5b-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="5fc5b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc5b-138">System.String</span></span>

## <span data-ttu-id="5fc5b-139">출력</span><span class="sxs-lookup"><span data-stu-id="5fc5b-139">OUTPUTS</span></span>

### <span data-ttu-id="5fc5b-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5fc5b-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="5fc5b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5fc5b-141">NOTES</span></span>

## <span data-ttu-id="5fc5b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fc5b-142">RELATED LINKS</span></span>
[<span data-ttu-id="5fc5b-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc5b-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
