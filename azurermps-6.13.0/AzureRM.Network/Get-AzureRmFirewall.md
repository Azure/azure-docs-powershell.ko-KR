---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711337"
---
# <span data-ttu-id="97f16-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="97f16-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="97f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97f16-102">SYNOPSIS</span></span>
<span data-ttu-id="97f16-103">Azure 방화벽을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97f16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97f16-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97f16-105">설명은</span><span class="sxs-lookup"><span data-stu-id="97f16-105">DESCRIPTION</span></span>
<span data-ttu-id="97f16-106">**AzureRmFirewall** cmdlet은 리소스 그룹에 하나 이상의 방화벽을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="97f16-107">예제의</span><span class="sxs-lookup"><span data-stu-id="97f16-107">EXAMPLES</span></span>

### <span data-ttu-id="97f16-108">1: 리소스 그룹의 모든 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="97f16-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="97f16-109">이 예제에서는 "rgName" 리소스 그룹의 모든 방화벽을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="97f16-110">2: 이름으로 방화벽 검색</span><span class="sxs-lookup"><span data-stu-id="97f16-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="97f16-111">이 예제에서는 "azFw" 이라고 하는 "rgName" 리소스 그룹의 방화벽을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="97f16-112">3: 방화벽을 검색 한 다음 응용 프로그램 규칙 컬렉션을 방화벽에 추가</span><span class="sxs-lookup"><span data-stu-id="97f16-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="97f16-113">이 예제에서는 방화벽을 검색 한 다음 메서드 AddApplicationRuleCollection를 호출 하 여 방화벽에 응용 프로그램 규칙 컬렉션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="97f16-114">4: 방화벽을 검색 한 다음 네트워크 규칙 컬렉션을 방화벽에 추가</span><span class="sxs-lookup"><span data-stu-id="97f16-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="97f16-115">이 예제에서는 방화벽을 검색 한 다음 메서드 AddNetworkRuleCollection를 호출 하 여 네트워크 규칙 컬렉션을 방화벽에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="97f16-116">5: 방화벽을 검색 한 다음 방화벽에서 이름으로 응용 프로그램 규칙 컬렉션 검색</span><span class="sxs-lookup"><span data-stu-id="97f16-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="97f16-117">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 가져옵니다. 방화벽 개체의 GetApplicationRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="97f16-118">메서드 GetApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="97f16-119">6: 방화벽을 검색 한 다음 방화벽에서 이름별로 네트워크 규칙 컬렉션 검색</span><span class="sxs-lookup"><span data-stu-id="97f16-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="97f16-120">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 가져옵니다. 방화벽 개체의 GetNetworkRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="97f16-121">메서드 GetNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="97f16-122">7: 방화벽을 검색 한 다음 방화벽에서 이름으로 응용 프로그램 규칙 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="97f16-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="97f16-123">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 제거 하 고 방화벽 개체의 RemoveApplicationRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="97f16-124">메서드 RemoveApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="97f16-125">8: 방화벽을 검색 한 다음 방화벽에서 이름으로 네트워크 규칙 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="97f16-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="97f16-126">이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 제거 하 고 방화벽 개체의 RemoveNetworkRuleCollectionByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="97f16-127">메서드 RemoveNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="97f16-128">9: 방화벽을 검색 한 다음 방화벽을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="97f16-129">이 예제에서는 방화벽을 검색 하 고 방화벽에 할당을 호출 하 여 방화벽과 연결 된 구성 (응용 프로그램 및 네트워크 규칙 컬렉션)을 사용 하 여 방화벽 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="97f16-130">변수</span><span class="sxs-lookup"><span data-stu-id="97f16-130">PARAMETERS</span></span>

### <span data-ttu-id="97f16-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f16-131">-DefaultProfile</span></span>
<span data-ttu-id="97f16-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97f16-133">-이름</span><span class="sxs-lookup"><span data-stu-id="97f16-133">-Name</span></span>
<span data-ttu-id="97f16-134">이 cmdlet이 가져오는 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f16-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f16-135">-ResourceGroupName</span></span>
<span data-ttu-id="97f16-136">방화벽이 속해 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f16-137">CommonParameters</span></span>
<span data-ttu-id="97f16-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f16-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f16-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f16-140">입력</span><span class="sxs-lookup"><span data-stu-id="97f16-140">INPUTS</span></span>

### <span data-ttu-id="97f16-141">않아야</span><span class="sxs-lookup"><span data-stu-id="97f16-141">None</span></span>
<span data-ttu-id="97f16-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97f16-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97f16-143">출력</span><span class="sxs-lookup"><span data-stu-id="97f16-143">OUTPUTS</span></span>

### <span data-ttu-id="97f16-144">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="97f16-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="97f16-145">상속자</span><span class="sxs-lookup"><span data-stu-id="97f16-145">NOTES</span></span>

## <span data-ttu-id="97f16-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97f16-146">RELATED LINKS</span></span>

[<span data-ttu-id="97f16-147">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="97f16-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="97f16-148">제거-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="97f16-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="97f16-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="97f16-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
