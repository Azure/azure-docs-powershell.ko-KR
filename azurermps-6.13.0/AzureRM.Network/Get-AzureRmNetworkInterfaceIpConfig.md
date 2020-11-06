---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: eac8a985cfcb531247fcf2617fee86da92ea0112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537992"
---
# <span data-ttu-id="8af07-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8af07-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="8af07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af07-102">SYNOPSIS</span></span>
<span data-ttu-id="8af07-103">네트워크 인터페이스에 대 한 네트워크 인터페이스 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8af07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8af07-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8af07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8af07-105">DESCRIPTION</span></span>
<span data-ttu-id="8af07-106">**AzureRmNetworkInterfaceIPConfig** Cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="8af07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8af07-107">EXAMPLES</span></span>

### <span data-ttu-id="8af07-108">1: 네트워크 인터페이스의 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8af07-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="8af07-109">첫 번째 명령은 mynic 이라는 기존 네트워크 인터페이스를 가져와이를 변수 $nic 1에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="8af07-110">두 번째 명령은이 네트워크 인터페이스의 ipconfig1 이라는 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="8af07-111">변수</span><span class="sxs-lookup"><span data-stu-id="8af07-111">PARAMETERS</span></span>

### <span data-ttu-id="8af07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af07-112">-DefaultProfile</span></span>
<span data-ttu-id="8af07-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af07-114">-이름</span><span class="sxs-lookup"><span data-stu-id="8af07-114">-Name</span></span>
<span data-ttu-id="8af07-115">이 cmdlet이 가져오는 네트워크 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8af07-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8af07-116">-NetworkInterface</span></span>
<span data-ttu-id="8af07-117">이 cmdlet이 가져오는 네트워크 IP 구성을 포함 하는 **NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8af07-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af07-118">CommonParameters</span></span>
<span data-ttu-id="8af07-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af07-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af07-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af07-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af07-121">입력</span><span class="sxs-lookup"><span data-stu-id="8af07-121">INPUTS</span></span>

### <span data-ttu-id="8af07-122">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8af07-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="8af07-123">매개 변수: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8af07-123">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="8af07-124">출력</span><span class="sxs-lookup"><span data-stu-id="8af07-124">OUTPUTS</span></span>

### <span data-ttu-id="8af07-125">PSNetworkInterfaceIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8af07-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="8af07-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8af07-126">NOTES</span></span>
* <span data-ttu-id="8af07-127">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="8af07-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8af07-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8af07-128">RELATED LINKS</span></span>

[<span data-ttu-id="8af07-129">추가-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8af07-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8af07-130">새로운 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8af07-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8af07-131">제거-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8af07-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8af07-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8af07-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


