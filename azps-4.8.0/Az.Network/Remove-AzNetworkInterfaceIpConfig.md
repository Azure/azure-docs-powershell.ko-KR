---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203925"
---
# <span data-ttu-id="4c4d9-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c4d9-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="4c4d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4d9-103">네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="4c4d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c4d9-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c4d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4c4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="4c4d9-106">**AzNetworkInterfaceIpConfig** Cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="4c4d9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4c4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="4c4d9-108">예제 1: 네트워크 인터페이스에서 IP 구성 삭제</span><span class="sxs-lookup"><span data-stu-id="4c4d9-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="4c4d9-109">첫 번째 명령은 mynic 이라는 네트워크 인터페이스를 가져와이를 변수 $nic에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="4c4d9-110">두 번째 명령은이 네트워크 인터페이스에 연결 된 IPConfig-1 이라는 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="4c4d9-111">세 번째 명령은 네트워크 인터페이스에 대 한 변경 내용을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="4c4d9-112">변수</span><span class="sxs-lookup"><span data-stu-id="4c4d9-112">PARAMETERS</span></span>

### <span data-ttu-id="4c4d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4d9-113">-DefaultProfile</span></span>
<span data-ttu-id="4c4d9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c4d9-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4c4d9-115">-Name</span></span>
<span data-ttu-id="4c4d9-116">제거할 네트워크 인터페이스 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="4c4d9-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4c4d9-117">-NetworkInterface</span></span>
<span data-ttu-id="4c4d9-118">**NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="4c4d9-119">이 개체는 제거할 네트워크 인터페이스 IP 구성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="4c4d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4d9-120">CommonParameters</span></span>
<span data-ttu-id="4c4d9-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4d9-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4d9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4d9-123">입력</span><span class="sxs-lookup"><span data-stu-id="4c4d9-123">INPUTS</span></span>

### <span data-ttu-id="4c4d9-124">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4c4d9-125">출력</span><span class="sxs-lookup"><span data-stu-id="4c4d9-125">OUTPUTS</span></span>

### <span data-ttu-id="4c4d9-126">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4c4d9-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4c4d9-127">상속자</span><span class="sxs-lookup"><span data-stu-id="4c4d9-127">NOTES</span></span>
* <span data-ttu-id="4c4d9-128">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="4c4d9-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4c4d9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c4d9-129">RELATED LINKS</span></span>

[<span data-ttu-id="4c4d9-130">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c4d9-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4c4d9-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c4d9-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4c4d9-132">새로운 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c4d9-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4c4d9-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c4d9-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


