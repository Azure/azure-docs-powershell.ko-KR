---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990948"
---
# <span data-ttu-id="89d43-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="89d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d43-102">SYNOPSIS</span></span>
<span data-ttu-id="89d43-103">공용 IP 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-103">Updates a public IP address.</span></span>

## <span data-ttu-id="89d43-104">구문</span><span class="sxs-lookup"><span data-stu-id="89d43-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89d43-105">설명</span><span class="sxs-lookup"><span data-stu-id="89d43-105">DESCRIPTION</span></span>
<span data-ttu-id="89d43-106">**Set-AzPublicIpAddress** cmdlet은 공용 IP 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="89d43-107">예제</span><span class="sxs-lookup"><span data-stu-id="89d43-107">EXAMPLES</span></span>

### <span data-ttu-id="89d43-108">1: 공용 IP 주소의 할당 방법 변경</span><span class="sxs-lookup"><span data-stu-id="89d43-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="89d43-109">첫 번째 명령은 리소스 그룹에서 이름과 함께 $publicIPName IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="89d43-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="89d43-110">두 번째 명령은 공용 IP 주소 개체의 할당 메서드를 "정적"으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="89d43-111">Set-AzPublicIPAddress 업데이트된 개체로 공용 IP 주소 리소스를 업데이트하고 할당 메서드를 'Static'으로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="89d43-112">공용 IP 주소가 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="89d43-113">2: 공용 IP 주소의 DNS 도메인 레이블 추가</span><span class="sxs-lookup"><span data-stu-id="89d43-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="89d43-114">첫 번째 명령은 리소스 그룹에서 이름과 함께 $publicIPName IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="89d43-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="89d43-115">두 번째 명령은 DomainNameLabel 속성을 필요한 dns 연결로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="89d43-116">Set-AzPublicIPAddress 명령은 업데이트된 개체로 공용 IP 주소 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="89d43-117">DomainNameLabel & Fqdn은 예상대로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="89d43-118">3: 공용 IP 주소의 DNS 도메인 레이블 변경</span><span class="sxs-lookup"><span data-stu-id="89d43-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="89d43-119">첫 번째 명령은 리소스 그룹에서 이름과 함께 $publicIPName IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="89d43-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="89d43-120">두 번째 명령은 DomainNameLabel 속성을 필요한 dns 연결로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="89d43-121">Set-AzPublicIPAddress 명령은 업데이트된 개체로 공용 IP 주소 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="89d43-122">DomainNameLabel & Fqdn은 예상대로 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="89d43-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="89d43-123">PARAMETERS</span></span>

### <span data-ttu-id="89d43-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89d43-124">-AsJob</span></span>
<span data-ttu-id="89d43-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="89d43-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89d43-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d43-126">-DefaultProfile</span></span>
<span data-ttu-id="89d43-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89d43-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-128">-PublicIpAddress</span></span>
<span data-ttu-id="89d43-129">공용 IP 주소를 설정해야 하는 상태를 나타내는 공용 IP 주소 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="89d43-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d43-130">CommonParameters</span></span>
<span data-ttu-id="89d43-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89d43-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d43-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="89d43-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d43-133">입력</span><span class="sxs-lookup"><span data-stu-id="89d43-133">INPUTS</span></span>

### <span data-ttu-id="89d43-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="89d43-135">출력</span><span class="sxs-lookup"><span data-stu-id="89d43-135">OUTPUTS</span></span>

### <span data-ttu-id="89d43-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="89d43-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89d43-137">NOTES</span></span>

## <span data-ttu-id="89d43-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89d43-138">RELATED LINKS</span></span>

[<span data-ttu-id="89d43-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="89d43-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="89d43-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89d43-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


