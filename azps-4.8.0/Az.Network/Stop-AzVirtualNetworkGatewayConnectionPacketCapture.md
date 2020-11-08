---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203858"
---
# <span data-ttu-id="2c4f9-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c4f9-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="2c4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4f9-103">가상 네트워크 게이트웨이 연결의 패킷 캡처 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="2c4f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c4f9-104">SYNTAX</span></span>

### <span data-ttu-id="2c4f9-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c4f9-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4f9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c4f9-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4f9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4f9-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c4f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c4f9-108">DESCRIPTION</span></span>
<span data-ttu-id="2c4f9-109">가상 네트워크 게이트웨이 연결에 대 한 패킷 캡처 작업을 중지 하 고 지정 된 저장소 컨테이너 SasUrl의 결과를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="2c4f9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2c4f9-110">EXAMPLES</span></span>

### <span data-ttu-id="2c4f9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c4f9-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="2c4f9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2c4f9-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="2c4f9-113">변수</span><span class="sxs-lookup"><span data-stu-id="2c4f9-113">PARAMETERS</span></span>

### <span data-ttu-id="2c4f9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c4f9-114">-AsJob</span></span>
<span data-ttu-id="2c4f9-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2c4f9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c4f9-116">-확인</span><span class="sxs-lookup"><span data-stu-id="2c4f9-116">-Confirm</span></span>
<span data-ttu-id="2c4f9-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4f9-118">-DefaultProfile</span></span>
<span data-ttu-id="2c4f9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c4f9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c4f9-120">-InputObject</span></span>
<span data-ttu-id="2c4f9-121">패킷 캡처가 시작 될 가상 네트워크 게이트웨이 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-121">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c4f9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2c4f9-122">-Name</span></span>
<span data-ttu-id="2c4f9-123">패킷 캡처를 시작할 가상 네트워크 게이트웨이 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c4f9-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-125">The resource group name.</span></span>

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

### <span data-ttu-id="2c4f9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4f9-126">-ResourceId</span></span>
<span data-ttu-id="2c4f9-127">패킷 캡처가 시작 되는 VirtualNetworkGatewayConnection의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="2c4f9-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="2c4f9-128">-SasUrl</span></span>
<span data-ttu-id="2c4f9-129">가상 네트워크 게이트웨이에서 중지 패킷 캡처에 대 한 SAS Url입니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="2c4f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4f9-130">-WhatIf</span></span>
<span data-ttu-id="2c4f9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c4f9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4f9-133">CommonParameters</span></span>
<span data-ttu-id="2c4f9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4f9-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4f9-136">입력</span><span class="sxs-lookup"><span data-stu-id="2c4f9-136">INPUTS</span></span>

### <span data-ttu-id="2c4f9-137">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="2c4f9-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c4f9-138">System.String</span></span>

## <span data-ttu-id="2c4f9-139">출력</span><span class="sxs-lookup"><span data-stu-id="2c4f9-139">OUTPUTS</span></span>

### <span data-ttu-id="2c4f9-140">PSVirtualNetworkGatewayPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2c4f9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="2c4f9-141">NOTES</span></span>

## <span data-ttu-id="2c4f9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c4f9-142">RELATED LINKS</span></span>
[<span data-ttu-id="2c4f9-143">시작-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c4f9-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)