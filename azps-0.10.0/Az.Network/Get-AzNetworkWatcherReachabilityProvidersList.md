---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875545"
---
# <span data-ttu-id="1bb8b-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1bb8b-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="1bb8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb8b-103">지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="1bb8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bb8b-104">SYNTAX</span></span>

### <span data-ttu-id="1bb8b-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1bb8b-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bb8b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1bb8b-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bb8b-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb8b-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bb8b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1bb8b-108">DESCRIPTION</span></span>
<span data-ttu-id="1bb8b-109">Get-AzNetworkWatcherReachabilityProvidersList에는 지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="1bb8b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1bb8b-110">EXAMPLES</span></span>

### <span data-ttu-id="1bb8b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1bb8b-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="1bb8b-112">미국 내에서 Azure Data Center에 대해 시애틀에 있는 사용 가능한 모든 공급자 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="1bb8b-113">변수</span><span class="sxs-lookup"><span data-stu-id="1bb8b-113">PARAMETERS</span></span>

### <span data-ttu-id="1bb8b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bb8b-114">-AsJob</span></span>
<span data-ttu-id="1bb8b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1bb8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bb8b-116">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="1bb8b-116">-City</span></span>
<span data-ttu-id="1bb8b-117">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-118">-국가</span><span class="sxs-lookup"><span data-stu-id="1bb8b-118">-Country</span></span>
<span data-ttu-id="1bb8b-119">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb8b-120">-DefaultProfile</span></span>
<span data-ttu-id="1bb8b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb8b-122">-위치</span><span class="sxs-lookup"><span data-stu-id="1bb8b-122">-Location</span></span>
<span data-ttu-id="1bb8b-123">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-123">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bb8b-124">-NetworkWatcher</span></span>
<span data-ttu-id="1bb8b-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="1bb8b-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1bb8b-126">-NetworkWatcherName</span></span>
<span data-ttu-id="1bb8b-127">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb8b-128">-ResourceGroupName</span></span>
<span data-ttu-id="1bb8b-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb8b-130">-ResourceId</span></span>
<span data-ttu-id="1bb8b-131">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-131">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-132">-상태</span><span class="sxs-lookup"><span data-stu-id="1bb8b-132">-State</span></span>
<span data-ttu-id="1bb8b-133">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-133">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb8b-134">CommonParameters</span></span>
<span data-ttu-id="1bb8b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb8b-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb8b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb8b-137">입력</span><span class="sxs-lookup"><span data-stu-id="1bb8b-137">INPUTS</span></span>

### <span data-ttu-id="1bb8b-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bb8b-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1bb8b-139">4.0.0.0 ' 1 [[시스템 문자열, mscorlib, Version =, Culture = 중립, PublicKeyToken = b77a5c561934e089]] 목록</span><span class="sxs-lookup"><span data-stu-id="1bb8b-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1bb8b-140">출력</span><span class="sxs-lookup"><span data-stu-id="1bb8b-140">OUTPUTS</span></span>

### <span data-ttu-id="1bb8b-141">PSAvailableProvidersList에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="1bb8b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1bb8b-142">NOTES</span></span>
<span data-ttu-id="1bb8b-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="1bb8b-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="1bb8b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bb8b-144">RELATED LINKS</span></span>

[<span data-ttu-id="1bb8b-145">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bb8b-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1bb8b-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bb8b-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1bb8b-147">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bb8b-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1bb8b-148">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1bb8b-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1bb8b-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1bb8b-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1bb8b-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1bb8b-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1bb8b-151">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1bb8b-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1bb8b-152">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bb8b-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bb8b-153">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1bb8b-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1bb8b-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bb8b-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bb8b-155">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bb8b-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bb8b-156">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bb8b-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
