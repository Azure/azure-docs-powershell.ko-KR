---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495115"
---
# <span data-ttu-id="00732-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="00732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00732-102">SYNOPSIS</span></span>
<span data-ttu-id="00732-103">공용 IP 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-103">Updates a public IP address.</span></span>

## <span data-ttu-id="00732-104">구문</span><span class="sxs-lookup"><span data-stu-id="00732-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00732-105">설명</span><span class="sxs-lookup"><span data-stu-id="00732-105">DESCRIPTION</span></span>
<span data-ttu-id="00732-106">**Set-AzPublicIpAddress** cmdlet은 공용 IP 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="00732-107">예제</span><span class="sxs-lookup"><span data-stu-id="00732-107">EXAMPLES</span></span>

### <span data-ttu-id="00732-108">1: 공용 IP 주소의 할당 방법 변경</span><span class="sxs-lookup"><span data-stu-id="00732-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="00732-109">첫 번째 명령은 리소스 그룹에서 이름이 $publicIPName 공용 IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="00732-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="00732-110">두 번째 명령은 공용 IP 주소 개체의 할당 메서드를 "고정"으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="00732-111">Set-AzPublicIPAddress 업데이트된 개체로 공용 IP 주소 리소스를 업데이트하고 할당 메서드를 '고정'으로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="00732-112">공용 IP 주소는 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="00732-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="00732-113">2: 공용 IP 주소의 DNS 도메인 레이블 추가</span><span class="sxs-lookup"><span data-stu-id="00732-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="00732-114">첫 번째 명령은 리소스 그룹에서 이름이 $publicIPName 공용 IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="00732-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="00732-115">두 번째 명령은 DomainNameLabel 속성을 필요한 dns prefix로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="00732-116">Set-AzPublicIPAddress 업데이트된 개체로 공용 IP 주소 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="00732-117">DomainNameLabel & Fqdn이 예상대로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="00732-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="00732-118">3: 공용 IP 주소의 DNS 도메인 레이블 변경</span><span class="sxs-lookup"><span data-stu-id="00732-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="00732-119">첫 번째 명령은 리소스 그룹에서 이름이 $publicIPName 공용 IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="00732-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="00732-120">두 번째 명령은 DomainNameLabel 속성을 필요한 dns prefix로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="00732-121">Set-AzPublicIPAddress 업데이트된 개체로 공용 IP 주소 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="00732-122">DomainNameLabel & Fqdn이 예상대로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="00732-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="00732-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00732-123">PARAMETERS</span></span>

### <span data-ttu-id="00732-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00732-124">-AsJob</span></span>
<span data-ttu-id="00732-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="00732-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00732-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00732-126">-DefaultProfile</span></span>
<span data-ttu-id="00732-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00732-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00732-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-128">-PublicIpAddress</span></span>
<span data-ttu-id="00732-129">공용 IP 주소를 설정해야 하는 상태를 나타내는 공용 IP 주소 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00732-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00732-130">CommonParameters</span></span>
<span data-ttu-id="00732-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00732-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00732-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="00732-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00732-133">입력</span><span class="sxs-lookup"><span data-stu-id="00732-133">INPUTS</span></span>

### <span data-ttu-id="00732-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="00732-135">출력</span><span class="sxs-lookup"><span data-stu-id="00732-135">OUTPUTS</span></span>

### <span data-ttu-id="00732-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="00732-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00732-137">NOTES</span></span>

## <span data-ttu-id="00732-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00732-138">RELATED LINKS</span></span>

[<span data-ttu-id="00732-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="00732-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="00732-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00732-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


