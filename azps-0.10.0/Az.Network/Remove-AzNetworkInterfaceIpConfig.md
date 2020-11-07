---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2ccb5f7117df8f959698c894915cedd3a5d4c7e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875325"
---
# <span data-ttu-id="800b1-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800b1-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="800b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="800b1-102">SYNOPSIS</span></span>
<span data-ttu-id="800b1-103">네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="800b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="800b1-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="800b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="800b1-105">DESCRIPTION</span></span>
<span data-ttu-id="800b1-106">**AzNetworkInterfaceIpConfig** Cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="800b1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="800b1-107">EXAMPLES</span></span>

### <span data-ttu-id="800b1-108">1: 네트워크 인터페이스에서 IP 구성 삭제</span><span class="sxs-lookup"><span data-stu-id="800b1-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="800b1-109">첫 번째 명령은 mynic 이라는 네트워크 인터페이스를 가져와이를 변수 $nic에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="800b1-110">두 번째 명령은이 네트워크 인터페이스에 연결 된 IPConfig-1 이라는 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="800b1-111">변수</span><span class="sxs-lookup"><span data-stu-id="800b1-111">PARAMETERS</span></span>

### <span data-ttu-id="800b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800b1-112">-DefaultProfile</span></span>
<span data-ttu-id="800b1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800b1-114">-이름</span><span class="sxs-lookup"><span data-stu-id="800b1-114">-Name</span></span>
<span data-ttu-id="800b1-115">제거할 네트워크 인터페이스 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800b1-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="800b1-116">-NetworkInterface</span></span>
<span data-ttu-id="800b1-117">**NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="800b1-118">이 개체는 제거할 네트워크 인터페이스 IP 구성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="800b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800b1-119">CommonParameters</span></span>
<span data-ttu-id="800b1-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800b1-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800b1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800b1-122">입력</span><span class="sxs-lookup"><span data-stu-id="800b1-122">INPUTS</span></span>

### <span data-ttu-id="800b1-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="800b1-123">PSNetworkInterface</span></span>
<span data-ttu-id="800b1-124">' NetworkInterface ' 매개 변수는 파이프라인에서 ' PSNetworkInterface ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="800b1-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="800b1-125">출력</span><span class="sxs-lookup"><span data-stu-id="800b1-125">OUTPUTS</span></span>

### <span data-ttu-id="800b1-126">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="800b1-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="800b1-127">상속자</span><span class="sxs-lookup"><span data-stu-id="800b1-127">NOTES</span></span>
* <span data-ttu-id="800b1-128">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="800b1-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="800b1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="800b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="800b1-130">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800b1-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="800b1-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800b1-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="800b1-132">새로운 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800b1-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="800b1-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800b1-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


