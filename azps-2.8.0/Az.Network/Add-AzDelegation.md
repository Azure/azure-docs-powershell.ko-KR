---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: e7646ff4a52131aaf1468cf32534235f71e7bf7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870889"
---
# <span data-ttu-id="cc5fc-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="cc5fc-101">Add-AzDelegation</span></span>

## <span data-ttu-id="cc5fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5fc-103">서브넷에 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="cc5fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc5fc-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc5fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="cc5fc-106">**Add-AzDelegation** Cmdlet은 Azure 서브넷에 서비스 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="cc5fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="cc5fc-108">1: 위임 추가</span><span class="sxs-lookup"><span data-stu-id="cc5fc-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="cc5fc-109">첫 번째 명령은 서브넷이 위치한 가상 네트워크를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="cc5fc-110">두 번째 명령은 위임 하려는 서브넷을 격리 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="cc5fc-111">세 번째 명령은 서브넷에 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="cc5fc-112">이 특정 예는이 서브넷에서 SQL이 인터페이스 끝점을 만들 수 있도록 설정 하려는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="cc5fc-113">마지막 명령은 서브넷을 실제로 업데이트 하기 위해 업데이트 된 서브넷을 서버에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="cc5fc-114">변수</span><span class="sxs-lookup"><span data-stu-id="cc5fc-114">PARAMETERS</span></span>

### <span data-ttu-id="cc5fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5fc-115">-DefaultProfile</span></span>
<span data-ttu-id="cc5fc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5fc-117">-이름</span><span class="sxs-lookup"><span data-stu-id="cc5fc-117">-Name</span></span>
<span data-ttu-id="cc5fc-118">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-118">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5fc-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc5fc-119">-ServiceName</span></span>
<span data-ttu-id="cc5fc-120">서브넷을 위임할 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5fc-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="cc5fc-121">-Subnet</span></span>
<span data-ttu-id="cc5fc-122">서브넷</span><span class="sxs-lookup"><span data-stu-id="cc5fc-122">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5fc-123">CommonParameters</span></span>
<span data-ttu-id="cc5fc-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5fc-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5fc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5fc-126">입력</span><span class="sxs-lookup"><span data-stu-id="cc5fc-126">INPUTS</span></span>

### <span data-ttu-id="cc5fc-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc5fc-127">System.String</span></span>

### <span data-ttu-id="cc5fc-128">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc5fc-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cc5fc-129">출력</span><span class="sxs-lookup"><span data-stu-id="cc5fc-129">OUTPUTS</span></span>

### <span data-ttu-id="cc5fc-130">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cc5fc-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cc5fc-131">상속자</span><span class="sxs-lookup"><span data-stu-id="cc5fc-131">NOTES</span></span>

## <span data-ttu-id="cc5fc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc5fc-132">RELATED LINKS</span></span>

<span data-ttu-id="cc5fc-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="cc5fc-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>