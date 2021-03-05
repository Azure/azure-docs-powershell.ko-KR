---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 0f5cedd29b7dcc296494519fe40f8ea7e0edb445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964251"
---
# <span data-ttu-id="116f7-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="116f7-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="116f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116f7-102">SYNOPSIS</span></span>
<span data-ttu-id="116f7-103">가상 네트워크 게이트웨이 연결의 IKE 보안 협회를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="116f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="116f7-104">SYNTAX</span></span>

### <span data-ttu-id="116f7-105">ByName</span><span class="sxs-lookup"><span data-stu-id="116f7-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="116f7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="116f7-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="116f7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="116f7-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="116f7-108">설명</span><span class="sxs-lookup"><span data-stu-id="116f7-108">DESCRIPTION</span></span>
<span data-ttu-id="116f7-109">**Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet은 연결 이름 및 리소스 그룹 이름을 기반으로 연결의 IKE 보안 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="116f7-110">-Name 매개 변수를 지정하지 않고 **Get-AzVirtualNetworkGatewayConnection** cmdlet이 발급되면 출력에 IKE 보안 협회가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="116f7-111">예제</span><span class="sxs-lookup"><span data-stu-id="116f7-111">EXAMPLES</span></span>

### <span data-ttu-id="116f7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="116f7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="116f7-113">리소스 그룹 "myRG" 내에서 "myTunnel"으로 가상 네트워크 게이트웨이 연결에 대한 IKE 보안 협회를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="116f7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="116f7-114">PARAMETERS</span></span>

### <span data-ttu-id="116f7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="116f7-115">-AsJob</span></span>
<span data-ttu-id="116f7-116">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="116f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116f7-117">-DefaultProfile</span></span>
<span data-ttu-id="116f7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="116f7-119">-InputObject</span></span>
<span data-ttu-id="116f7-120">IKE SAS를 페치해야 하는 가상 네트워크 게이트웨이 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116f7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="116f7-121">-Name</span></span>
<span data-ttu-id="116f7-122">IKE SAS를 페치해야 하는 가상 네트워크 게이트웨이 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="116f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="116f7-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="116f7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="116f7-125">-ResourceId</span></span>
<span data-ttu-id="116f7-126">IKE SAS를 페치해야 하는 Virtual Network Gateway 연결의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116f7-127">CommonParameters</span></span>
<span data-ttu-id="116f7-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="116f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116f7-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="116f7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116f7-130">입력</span><span class="sxs-lookup"><span data-stu-id="116f7-130">INPUTS</span></span>

### <span data-ttu-id="116f7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="116f7-131">System.String</span></span>

## <span data-ttu-id="116f7-132">출력</span><span class="sxs-lookup"><span data-stu-id="116f7-132">OUTPUTS</span></span>

### <span data-ttu-id="116f7-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="116f7-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="116f7-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="116f7-134">NOTES</span></span>

## <span data-ttu-id="116f7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="116f7-135">RELATED LINKS</span></span>
