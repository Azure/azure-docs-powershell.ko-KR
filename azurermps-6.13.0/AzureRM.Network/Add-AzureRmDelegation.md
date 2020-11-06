---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534268"
---
# <span data-ttu-id="23747-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="23747-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="23747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23747-102">SYNOPSIS</span></span>
<span data-ttu-id="23747-103">서브넷에 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23747-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23747-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23747-105">설명은</span><span class="sxs-lookup"><span data-stu-id="23747-105">DESCRIPTION</span></span>
<span data-ttu-id="23747-106">**Add-AzureRmDelegation** Cmdlet은 Azure 서브넷에 서비스 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="23747-107">예제의</span><span class="sxs-lookup"><span data-stu-id="23747-107">EXAMPLES</span></span>

### <span data-ttu-id="23747-108">1: 위임 추가</span><span class="sxs-lookup"><span data-stu-id="23747-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="23747-109">첫 번째 명령은 서브넷이 위치한 가상 네트워크를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="23747-110">두 번째 명령은 위임 하려는 서브넷을 격리 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="23747-111">세 번째 명령은 서브넷에 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="23747-112">이 특정 예는이 서브넷에서 SQL이 인터페이스 끝점을 만들 수 있도록 설정 하려는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="23747-113">마지막 명령은 서브넷을 실제로 업데이트 하기 위해 업데이트 된 서브넷을 서버에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="23747-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="23747-114">변수</span><span class="sxs-lookup"><span data-stu-id="23747-114">PARAMETERS</span></span>

### <span data-ttu-id="23747-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23747-115">-DefaultProfile</span></span>
<span data-ttu-id="23747-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23747-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23747-117">-이름</span><span class="sxs-lookup"><span data-stu-id="23747-117">-Name</span></span>
<span data-ttu-id="23747-118">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23747-118">The name of the delegation</span></span>

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

### <span data-ttu-id="23747-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="23747-119">-ServiceName</span></span>
<span data-ttu-id="23747-120">서브넷을 위임할 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23747-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23747-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="23747-121">-Subnet</span></span>
<span data-ttu-id="23747-122">서브넷</span><span class="sxs-lookup"><span data-stu-id="23747-122">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23747-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23747-123">CommonParameters</span></span>
<span data-ttu-id="23747-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23747-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="23747-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23747-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23747-126">입력</span><span class="sxs-lookup"><span data-stu-id="23747-126">INPUTS</span></span>

### <span data-ttu-id="23747-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23747-127">System.String</span></span>

### <span data-ttu-id="23747-128">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="23747-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="23747-129">출력</span><span class="sxs-lookup"><span data-stu-id="23747-129">OUTPUTS</span></span>

### <span data-ttu-id="23747-130">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="23747-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="23747-131">상속자</span><span class="sxs-lookup"><span data-stu-id="23747-131">NOTES</span></span>

## <span data-ttu-id="23747-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23747-132">RELATED LINKS</span></span>
<span data-ttu-id="23747-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="23747-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
