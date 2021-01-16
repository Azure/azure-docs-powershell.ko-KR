---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341666"
---
# <span data-ttu-id="4d5ba-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d5ba-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="4d5ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5ba-103">네트워크 인터페이스에 대한 네트워크 인터페이스 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="4d5ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d5ba-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d5ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="4d5ba-105">DESCRIPTION</span></span>
<span data-ttu-id="4d5ba-106">**Get-AzNetworkInterfaceIPConfig** cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="4d5ba-107">예제</span><span class="sxs-lookup"><span data-stu-id="4d5ba-107">EXAMPLES</span></span>

### <span data-ttu-id="4d5ba-108">1: 네트워크 인터페이스의 IP 구성을 갖기</span><span class="sxs-lookup"><span data-stu-id="4d5ba-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="4d5ba-109">첫 번째 명령은 mynic라는 기존 네트워크 인터페이스를 사용하여 변수 1에 $nic.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="4d5ba-110">두 번째 명령은 이 네트워크 인터페이스의 ipconfig1이라는 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="4d5ba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d5ba-111">PARAMETERS</span></span>

### <span data-ttu-id="4d5ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5ba-112">-DefaultProfile</span></span>
<span data-ttu-id="4d5ba-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d5ba-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4d5ba-114">-Name</span></span>
<span data-ttu-id="4d5ba-115">이 cmdlet에서 얻을 네트워크 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4d5ba-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4d5ba-116">-NetworkInterface</span></span>
<span data-ttu-id="4d5ba-117">이 cmdlet에서 얻을 네트워크 IP 구성을 포함하는 **NetworkInterface** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4d5ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5ba-118">CommonParameters</span></span>
<span data-ttu-id="4d5ba-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5ba-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d5ba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5ba-121">입력</span><span class="sxs-lookup"><span data-stu-id="4d5ba-121">INPUTS</span></span>

### <span data-ttu-id="4d5ba-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4d5ba-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4d5ba-123">출력</span><span class="sxs-lookup"><span data-stu-id="4d5ba-123">OUTPUTS</span></span>

### <span data-ttu-id="4d5ba-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d5ba-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="4d5ba-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d5ba-125">NOTES</span></span>
* <span data-ttu-id="4d5ba-126">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="4d5ba-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4d5ba-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d5ba-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d5ba-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d5ba-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d5ba-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d5ba-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d5ba-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d5ba-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d5ba-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d5ba-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


