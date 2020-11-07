---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 093a847154c75ee7c640bda522ebf16baa04560a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711703"
---
# <span data-ttu-id="b8e51-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8e51-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="b8e51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e51-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e51-103">지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8e51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8e51-104">SYNTAX</span></span>

### <span data-ttu-id="b8e51-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8e51-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8e51-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8e51-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8e51-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e51-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8e51-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b8e51-108">DESCRIPTION</span></span>
<span data-ttu-id="b8e51-109">Get-AzureRmNetworkWatcherReachabilityProvidersList에는 지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="b8e51-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8e51-110">EXAMPLES</span></span>

### <span data-ttu-id="b8e51-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8e51-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="b8e51-112">미국 내에서 Azure Data Center에 대해 시애틀에 있는 사용 가능한 모든 공급자 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="b8e51-113">변수</span><span class="sxs-lookup"><span data-stu-id="b8e51-113">PARAMETERS</span></span>

### <span data-ttu-id="b8e51-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8e51-114">-AsJob</span></span>
<span data-ttu-id="b8e51-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b8e51-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8e51-116">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="b8e51-116">-City</span></span>
<span data-ttu-id="b8e51-117">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-117">The name of the city.</span></span>

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

### <span data-ttu-id="b8e51-118">-국가</span><span class="sxs-lookup"><span data-stu-id="b8e51-118">-Country</span></span>
<span data-ttu-id="b8e51-119">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-119">The name of the country.</span></span>

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

### <span data-ttu-id="b8e51-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e51-120">-DefaultProfile</span></span>
<span data-ttu-id="b8e51-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8e51-122">-위치</span><span class="sxs-lookup"><span data-stu-id="b8e51-122">-Location</span></span>
<span data-ttu-id="b8e51-123">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="b8e51-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8e51-124">-NetworkWatcher</span></span>
<span data-ttu-id="b8e51-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="b8e51-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="b8e51-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b8e51-126">-NetworkWatcherName</span></span>
<span data-ttu-id="b8e51-127">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="b8e51-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e51-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8e51-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b8e51-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e51-130">-ResourceId</span></span>
<span data-ttu-id="b8e51-131">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="b8e51-132">-상태</span><span class="sxs-lookup"><span data-stu-id="b8e51-132">-State</span></span>
<span data-ttu-id="b8e51-133">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-133">The name of the state.</span></span>

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

### <span data-ttu-id="b8e51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e51-134">CommonParameters</span></span>
<span data-ttu-id="b8e51-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e51-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e51-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e51-137">입력</span><span class="sxs-lookup"><span data-stu-id="b8e51-137">INPUTS</span></span>

### <span data-ttu-id="b8e51-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8e51-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b8e51-139">4.0.0.0 ' 1 [[시스템 문자열, mscorlib, Version =, Culture = 중립, PublicKeyToken = b77a5c561934e089]] 목록</span><span class="sxs-lookup"><span data-stu-id="b8e51-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b8e51-140">출력</span><span class="sxs-lookup"><span data-stu-id="b8e51-140">OUTPUTS</span></span>

### <span data-ttu-id="b8e51-141">PSAvailableProvidersList에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b8e51-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="b8e51-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b8e51-142">NOTES</span></span>
<span data-ttu-id="b8e51-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="b8e51-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="b8e51-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8e51-144">RELATED LINKS</span></span>

[<span data-ttu-id="b8e51-145">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8e51-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b8e51-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8e51-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b8e51-147">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8e51-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b8e51-148">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b8e51-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b8e51-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b8e51-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b8e51-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b8e51-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b8e51-151">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b8e51-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b8e51-152">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8e51-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8e51-153">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b8e51-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b8e51-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8e51-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8e51-155">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8e51-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8e51-156">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8e51-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
