---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204028"
---
# <span data-ttu-id="12941-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12941-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="12941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12941-102">SYNOPSIS</span></span>
<span data-ttu-id="12941-103">네트워크 인터페이스에 대 한 네트워크 인터페이스 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12941-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="12941-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12941-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12941-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12941-105">DESCRIPTION</span></span>
<span data-ttu-id="12941-106">**AzNetworkInterfaceIPConfig** Cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12941-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="12941-107">예제의</span><span class="sxs-lookup"><span data-stu-id="12941-107">EXAMPLES</span></span>

### <span data-ttu-id="12941-108">1: 네트워크 인터페이스의 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="12941-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="12941-109">첫 번째 명령은 mynic 이라는 기존 네트워크 인터페이스를 가져와이를 변수 $nic 1에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="12941-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="12941-110">두 번째 명령은이 네트워크 인터페이스의 ipconfig1 이라는 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12941-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="12941-111">변수</span><span class="sxs-lookup"><span data-stu-id="12941-111">PARAMETERS</span></span>

### <span data-ttu-id="12941-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12941-112">-DefaultProfile</span></span>
<span data-ttu-id="12941-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12941-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12941-114">-이름</span><span class="sxs-lookup"><span data-stu-id="12941-114">-Name</span></span>
<span data-ttu-id="12941-115">이 cmdlet이 가져오는 네트워크 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12941-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12941-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="12941-116">-NetworkInterface</span></span>
<span data-ttu-id="12941-117">이 cmdlet이 가져오는 네트워크 IP 구성을 포함 하는 **NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12941-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12941-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12941-118">CommonParameters</span></span>
<span data-ttu-id="12941-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12941-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12941-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12941-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12941-121">입력</span><span class="sxs-lookup"><span data-stu-id="12941-121">INPUTS</span></span>

### <span data-ttu-id="12941-122">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="12941-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="12941-123">출력</span><span class="sxs-lookup"><span data-stu-id="12941-123">OUTPUTS</span></span>

### <span data-ttu-id="12941-124">PSNetworkInterfaceIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="12941-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="12941-125">상속자</span><span class="sxs-lookup"><span data-stu-id="12941-125">NOTES</span></span>
* <span data-ttu-id="12941-126">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="12941-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="12941-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12941-127">RELATED LINKS</span></span>

[<span data-ttu-id="12941-128">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12941-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="12941-129">새로운 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12941-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="12941-130">제거-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12941-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="12941-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12941-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


