---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 88cbb5417e8a82ede25cc77274294a5dc4f64b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203851"
---
# <span data-ttu-id="b8402-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8402-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="b8402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8402-102">SYNOPSIS</span></span>
<span data-ttu-id="b8402-103">Vpn 연결의 패킷 캡처 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="b8402-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8402-104">SYNTAX</span></span>

### <span data-ttu-id="b8402-105">ByVpnConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8402-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-LinkConnectionName <String>] -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8402-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b8402-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-LinkConnectionName <String>]
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8402-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b8402-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> [-LinkConnectionName <String>] -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8402-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b8402-108">DESCRIPTION</span></span>
<span data-ttu-id="b8402-109">Vpn 연결에서 패킷 캡처 작업을 중지 하 고 지정 된 저장소 컨테이너 SasUrl의 결과를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="b8402-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8402-110">EXAMPLES</span></span>

### <span data-ttu-id="b8402-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8402-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="b8402-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8402-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="b8402-113">변수</span><span class="sxs-lookup"><span data-stu-id="b8402-113">PARAMETERS</span></span>

### <span data-ttu-id="b8402-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8402-114">-AsJob</span></span>
<span data-ttu-id="b8402-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b8402-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8402-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8402-116">-DefaultProfile</span></span>
<span data-ttu-id="b8402-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8402-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8402-118">-InputObject</span></span>
<span data-ttu-id="b8402-119">패킷을 캡처 시작 하는 Vpn 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8402-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="b8402-120">-LinkConnectionName</span></span>
<span data-ttu-id="b8402-121">SiteLinkConnection의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-121">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8402-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b8402-122">-Name</span></span>
<span data-ttu-id="b8402-123">패킷 캡처를 시작할 Vpn 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8402-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b8402-124">-ParentResourceName</span></span>
<span data-ttu-id="b8402-125">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8402-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8402-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8402-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8402-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8402-128">-ResourceId</span></span>
<span data-ttu-id="b8402-129">패킷 캡처가 시작 되는 VpnConnection의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8402-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="b8402-130">-SasUrl</span></span>
<span data-ttu-id="b8402-131">Vpn의 중지 패킷 캡처에 대 한 SAS Url입니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="b8402-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b8402-132">-Confirm</span></span>
<span data-ttu-id="b8402-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8402-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8402-134">-WhatIf</span></span>
<span data-ttu-id="b8402-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8402-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8402-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8402-137">CommonParameters</span></span>
<span data-ttu-id="b8402-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8402-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8402-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8402-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8402-140">입력</span><span class="sxs-lookup"><span data-stu-id="b8402-140">INPUTS</span></span>

### <span data-ttu-id="b8402-141">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b8402-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="b8402-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8402-142">System.String</span></span>

## <span data-ttu-id="b8402-143">출력</span><span class="sxs-lookup"><span data-stu-id="b8402-143">OUTPUTS</span></span>

### <span data-ttu-id="b8402-144">PSVpnPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b8402-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="b8402-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b8402-145">NOTES</span></span>

## <span data-ttu-id="b8402-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8402-146">RELATED LINKS</span></span>

[<span data-ttu-id="b8402-147">시작-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8402-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)