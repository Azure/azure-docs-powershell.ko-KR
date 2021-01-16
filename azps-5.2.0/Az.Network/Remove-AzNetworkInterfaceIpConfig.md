---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333477"
---
# <span data-ttu-id="738ac-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ac-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="738ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="738ac-102">SYNOPSIS</span></span>
<span data-ttu-id="738ac-103">네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="738ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="738ac-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="738ac-105">설명</span><span class="sxs-lookup"><span data-stu-id="738ac-105">DESCRIPTION</span></span>
<span data-ttu-id="738ac-106">**Remove-AzNetworkInterfaceIpConfig** cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="738ac-107">예제</span><span class="sxs-lookup"><span data-stu-id="738ac-107">EXAMPLES</span></span>

### <span data-ttu-id="738ac-108">예제 1: 네트워크 인터페이스에서 IP 구성 삭제</span><span class="sxs-lookup"><span data-stu-id="738ac-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="738ac-109">첫 번째 명령은 mynic라는 네트워크 인터페이스를 사용하여 변수 인터페이스에 $nic.</span><span class="sxs-lookup"><span data-stu-id="738ac-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="738ac-110">두 번째 명령은 이 네트워크 인터페이스와 연결된 IPConfig-1이라는 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="738ac-111">세 번째 명령은 네트워크 인터페이스에 대한 변경 내용을 집합합니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="738ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="738ac-112">PARAMETERS</span></span>

### <span data-ttu-id="738ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738ac-113">-DefaultProfile</span></span>
<span data-ttu-id="738ac-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="738ac-115">-Name</span><span class="sxs-lookup"><span data-stu-id="738ac-115">-Name</span></span>
<span data-ttu-id="738ac-116">제거할 네트워크 인터페이스 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-116">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="738ac-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="738ac-117">-NetworkInterface</span></span>
<span data-ttu-id="738ac-118">**NetworkInterface 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="738ac-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="738ac-119">이 개체에는 제거할 네트워크 인터페이스 IP 구성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="738ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738ac-120">CommonParameters</span></span>
<span data-ttu-id="738ac-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="738ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738ac-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="738ac-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738ac-123">입력</span><span class="sxs-lookup"><span data-stu-id="738ac-123">INPUTS</span></span>

### <span data-ttu-id="738ac-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="738ac-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="738ac-125">출력</span><span class="sxs-lookup"><span data-stu-id="738ac-125">OUTPUTS</span></span>

### <span data-ttu-id="738ac-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="738ac-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="738ac-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="738ac-127">NOTES</span></span>
* <span data-ttu-id="738ac-128">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="738ac-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="738ac-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="738ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="738ac-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ac-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="738ac-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ac-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="738ac-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ac-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="738ac-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ac-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


