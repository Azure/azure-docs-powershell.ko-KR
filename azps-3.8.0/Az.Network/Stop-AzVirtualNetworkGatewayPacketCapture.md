---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034109"
---
# <span data-ttu-id="67afe-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67afe-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="67afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67afe-102">SYNOPSIS</span></span>
<span data-ttu-id="67afe-103">가상 네트워크 게이트웨이에서 패킷 캡처 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="67afe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67afe-104">SYNTAX</span></span>

### <span data-ttu-id="67afe-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="67afe-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67afe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67afe-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67afe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67afe-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67afe-108">설명은</span><span class="sxs-lookup"><span data-stu-id="67afe-108">DESCRIPTION</span></span>
<span data-ttu-id="67afe-109">가상 네트워크 게이트웨이에서 패킷 캡처 작업을 중지 하 고 지정 된 SasUrl 저장소 컨테이너에 대 한 결과를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="67afe-110">예제의</span><span class="sxs-lookup"><span data-stu-id="67afe-110">EXAMPLES</span></span>

### <span data-ttu-id="67afe-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="67afe-111">Example 1</span></span>
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

### <span data-ttu-id="67afe-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="67afe-112">Example 2</span></span>
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

## <span data-ttu-id="67afe-113">변수</span><span class="sxs-lookup"><span data-stu-id="67afe-113">PARAMETERS</span></span>

### <span data-ttu-id="67afe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67afe-114">-AsJob</span></span>
<span data-ttu-id="67afe-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="67afe-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67afe-116">-확인</span><span class="sxs-lookup"><span data-stu-id="67afe-116">-Confirm</span></span>
<span data-ttu-id="67afe-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67afe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67afe-118">-DefaultProfile</span></span>
<span data-ttu-id="67afe-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67afe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67afe-120">-InputObject</span></span>
<span data-ttu-id="67afe-121">패킷 캡처가 시작 될 가상 네트워크 게이트웨이 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="67afe-122">-이름</span><span class="sxs-lookup"><span data-stu-id="67afe-122">-Name</span></span>
<span data-ttu-id="67afe-123">패킷을 캡처를 시작할 가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="67afe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67afe-124">-ResourceGroupName</span></span>
<span data-ttu-id="67afe-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-125">The resource group name.</span></span>

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

### <span data-ttu-id="67afe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67afe-126">-ResourceId</span></span>
<span data-ttu-id="67afe-127">패킷 캡처가 시작 되는 VirtualNetworkGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="67afe-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="67afe-128">-SasUrl</span></span>
<span data-ttu-id="67afe-129">가상 네트워크 게이트웨이에서 SAS URL 패킷 캡처.</span><span class="sxs-lookup"><span data-stu-id="67afe-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="67afe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67afe-130">-WhatIf</span></span>
<span data-ttu-id="67afe-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67afe-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67afe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67afe-133">CommonParameters</span></span>
<span data-ttu-id="67afe-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67afe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67afe-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="67afe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67afe-136">입력</span><span class="sxs-lookup"><span data-stu-id="67afe-136">INPUTS</span></span>

### <span data-ttu-id="67afe-137">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="67afe-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="67afe-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67afe-138">System.String</span></span>

## <span data-ttu-id="67afe-139">출력</span><span class="sxs-lookup"><span data-stu-id="67afe-139">OUTPUTS</span></span>

### <span data-ttu-id="67afe-140">PSVirtualNetworkGatewayPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="67afe-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="67afe-141">상속자</span><span class="sxs-lookup"><span data-stu-id="67afe-141">NOTES</span></span>

## <span data-ttu-id="67afe-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67afe-142">RELATED LINKS</span></span>
[<span data-ttu-id="67afe-143">시작-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67afe-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
