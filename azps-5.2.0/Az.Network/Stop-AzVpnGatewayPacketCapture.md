---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363413"
---
# <span data-ttu-id="2638d-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2638d-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="2638d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2638d-102">SYNOPSIS</span></span>
<span data-ttu-id="2638d-103">Vpn Gateway에서 패킷 캡처 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="2638d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2638d-104">SYNTAX</span></span>

### <span data-ttu-id="2638d-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2638d-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2638d-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2638d-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2638d-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2638d-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2638d-108">설명</span><span class="sxs-lookup"><span data-stu-id="2638d-108">DESCRIPTION</span></span>
<span data-ttu-id="2638d-109">Vpn Gateway에서 패킷 캡처 작업을 중지하고 저장소 컨테이너의 주어진 SasUrl에 결과를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="2638d-110">예제</span><span class="sxs-lookup"><span data-stu-id="2638d-110">EXAMPLES</span></span>

### <span data-ttu-id="2638d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2638d-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="2638d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2638d-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="2638d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2638d-113">PARAMETERS</span></span>

### <span data-ttu-id="2638d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2638d-114">-AsJob</span></span>
<span data-ttu-id="2638d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2638d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2638d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2638d-116">-DefaultProfile</span></span>
<span data-ttu-id="2638d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2638d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2638d-118">-InputObject</span></span>
<span data-ttu-id="2638d-119">패킷 캡처를 시작할 Vpn Gateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-119">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2638d-120">-Name</span></span>
<span data-ttu-id="2638d-121">패킷 캡처를 시작할 Vpn Gateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-121">The Vpn Gateway name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2638d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2638d-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2638d-124">-ResourceId</span></span>
<span data-ttu-id="2638d-125">패킷 캡처를 시작할 VpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="2638d-126">-SasUrl</span></span>
<span data-ttu-id="2638d-127">VPN Gateway에서 SAS URL 패킷 캡처.</span><span class="sxs-lookup"><span data-stu-id="2638d-127">SAS URL packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2638d-128">-Confirm</span></span>
<span data-ttu-id="2638d-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2638d-130">-WhatIf</span></span>
<span data-ttu-id="2638d-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2638d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2638d-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2638d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2638d-133">CommonParameters</span></span>
<span data-ttu-id="2638d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2638d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2638d-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2638d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2638d-136">입력</span><span class="sxs-lookup"><span data-stu-id="2638d-136">INPUTS</span></span>

### <span data-ttu-id="2638d-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2638d-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2638d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2638d-138">System.String</span></span>

## <span data-ttu-id="2638d-139">출력</span><span class="sxs-lookup"><span data-stu-id="2638d-139">OUTPUTS</span></span>

### <span data-ttu-id="2638d-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2638d-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2638d-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2638d-141">NOTES</span></span>

## <span data-ttu-id="2638d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2638d-142">RELATED LINKS</span></span>

[<span data-ttu-id="2638d-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2638d-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)