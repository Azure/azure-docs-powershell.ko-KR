---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876556"
---
# <span data-ttu-id="b29fa-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b29fa-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="b29fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b29fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b29fa-103">공용 IP 주소에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="b29fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b29fa-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b29fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b29fa-105">DESCRIPTION</span></span>
<span data-ttu-id="b29fa-106">**AzPublicIpAddress** cmdlet은 공용 IP 주소에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="b29fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b29fa-107">EXAMPLES</span></span>

### <span data-ttu-id="b29fa-108">1: 공용 IP 주소의 배정 방법 변경</span><span class="sxs-lookup"><span data-stu-id="b29fa-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="b29fa-109">첫 번째 명령은 리소스 그룹 $rgName에서 이름이 $publicIPName 인 공용 IP 주소 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="b29fa-110">두 번째 명령은 공용 IP 주소 개체의 배정 방법을 "Static"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="b29fa-111">Set-AzPublicIPAddress 명령은 업데이트 된 개체로 공용 IP 주소 리소스를 업데이트 하 고 할당 메서드를 ' Static '으로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="b29fa-112">공용 IP 주소가 즉시 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="b29fa-113">2: 공용 IP 주소의 DNS 도메인 레이블 변경</span><span class="sxs-lookup"><span data-stu-id="b29fa-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="b29fa-114">첫 번째 명령은 리소스 그룹 $rgName에서 이름이 $publicIPName 인 공용 IP 주소 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="b29fa-115">두 번째 명령은 DomainNameLabel 속성을 필수 dns 접두사로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="b29fa-116">Set-AzPublicIPAddress 명령은 공용 IP 주소 리소스를 업데이트 된 개체로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="b29fa-117">DomainNameLabel & Fqdn이 예상 대로 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="b29fa-118">변수</span><span class="sxs-lookup"><span data-stu-id="b29fa-118">PARAMETERS</span></span>

### <span data-ttu-id="b29fa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b29fa-119">-AsJob</span></span>
<span data-ttu-id="b29fa-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b29fa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b29fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29fa-121">-DefaultProfile</span></span>
<span data-ttu-id="b29fa-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b29fa-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b29fa-123">-PublicIpAddress</span></span>
<span data-ttu-id="b29fa-124">공용 IP 주소를 설정 해야 하는 목표 상태를 나타내는 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b29fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29fa-125">CommonParameters</span></span>
<span data-ttu-id="b29fa-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29fa-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29fa-128">입력</span><span class="sxs-lookup"><span data-stu-id="b29fa-128">INPUTS</span></span>

### <span data-ttu-id="b29fa-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b29fa-129">PSPublicIpAddress</span></span>
<span data-ttu-id="b29fa-130">' PublicIpAddress ' 매개 변수는 파이프라인에서 ' PSPublicIpAddress ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29fa-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="b29fa-131">출력</span><span class="sxs-lookup"><span data-stu-id="b29fa-131">OUTPUTS</span></span>

### <span data-ttu-id="b29fa-132">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b29fa-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b29fa-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b29fa-133">NOTES</span></span>

## <span data-ttu-id="b29fa-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b29fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="b29fa-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b29fa-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="b29fa-136">새로운 AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b29fa-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="b29fa-137">제거-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b29fa-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


