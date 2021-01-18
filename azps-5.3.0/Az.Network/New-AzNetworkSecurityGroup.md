---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493210"
---
# <span data-ttu-id="f0b21-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f0b21-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="f0b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b21-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b21-103">네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-103">Creates a network security group.</span></span>

## <span data-ttu-id="f0b21-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0b21-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b21-105">설명</span><span class="sxs-lookup"><span data-stu-id="f0b21-105">DESCRIPTION</span></span>
<span data-ttu-id="f0b21-106">**New-AzNetworkSecurityGroup** cmdlet은 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="f0b21-107">예제</span><span class="sxs-lookup"><span data-stu-id="f0b21-107">EXAMPLES</span></span>

### <span data-ttu-id="f0b21-108">예제 1: 새 네트워크 보안 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="f0b21-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="f0b21-109">이 명령은 "westus" 위치에 있는 리소스 그룹 "rg1"에 "nsg1"이라는 새 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="f0b21-110">예제 2: 자세한 네트워크 보안 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="f0b21-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="f0b21-111">1단계: 인터넷에서 포트 3389로의 액세스를 허용하는 보안 규칙을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="f0b21-112">2단계: 인터넷에서 포트 80으로의 액세스를 허용하는 보안 규칙을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="f0b21-113">3단계: 위에서 만든 규칙을 NSG-FrontEnd라는 새 NSG에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="f0b21-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0b21-114">PARAMETERS</span></span>

### <span data-ttu-id="f0b21-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0b21-115">-AsJob</span></span>
<span data-ttu-id="f0b21-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f0b21-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0b21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b21-117">-DefaultProfile</span></span>
<span data-ttu-id="f0b21-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0b21-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f0b21-119">-Force</span></span>
<span data-ttu-id="f0b21-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0b21-121">-Location</span><span class="sxs-lookup"><span data-stu-id="f0b21-121">-Location</span></span>
<span data-ttu-id="f0b21-122">네트워크 보안 그룹을 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f0b21-123">-Name</span></span>
<span data-ttu-id="f0b21-124">만들 네트워크 보안 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b21-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0b21-126">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f0b21-127">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹에 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="f0b21-128">-SecurityRules</span></span>
<span data-ttu-id="f0b21-129">네트워크 보안 그룹에 만들 네트워크 보안 규칙 개체의 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0b21-130">-Tag</span></span>
<span data-ttu-id="f0b21-131">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f0b21-132">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f0b21-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0b21-133">-Confirm</span></span>
<span data-ttu-id="f0b21-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b21-135">-WhatIf</span></span>
<span data-ttu-id="f0b21-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f0b21-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b21-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b21-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b21-138">CommonParameters</span></span>
<span data-ttu-id="f0b21-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b21-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0b21-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b21-141">입력</span><span class="sxs-lookup"><span data-stu-id="f0b21-141">INPUTS</span></span>

### <span data-ttu-id="f0b21-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f0b21-142">System.String</span></span>

### <span data-ttu-id="f0b21-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="f0b21-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="f0b21-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0b21-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0b21-145">출력</span><span class="sxs-lookup"><span data-stu-id="f0b21-145">OUTPUTS</span></span>

### <span data-ttu-id="f0b21-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f0b21-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f0b21-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0b21-147">NOTES</span></span>

## <span data-ttu-id="f0b21-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0b21-148">RELATED LINKS</span></span>

[<span data-ttu-id="f0b21-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f0b21-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="f0b21-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f0b21-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="f0b21-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f0b21-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
