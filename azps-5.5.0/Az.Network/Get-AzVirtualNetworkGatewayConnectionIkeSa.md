---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179804"
---
# <span data-ttu-id="21605-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="21605-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="21605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21605-102">SYNOPSIS</span></span>
<span data-ttu-id="21605-103">Virtual Network 게이트웨이 연결의 IKE 보안 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="21605-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="21605-104">구문</span><span class="sxs-lookup"><span data-stu-id="21605-104">SYNTAX</span></span>

### <span data-ttu-id="21605-105">ByName</span><span class="sxs-lookup"><span data-stu-id="21605-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21605-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="21605-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21605-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21605-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21605-108">설명</span><span class="sxs-lookup"><span data-stu-id="21605-108">DESCRIPTION</span></span>
<span data-ttu-id="21605-109">**Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet은 연결 이름 및 리소스 그룹 이름에 따라 연결의 IKE 보안 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21605-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="21605-110">-Name 매개 변수를 지정하지 않고 **Get-AzVirtualNetworkGatewayConnection** cmdlet을 발급하면 출력에 IKE 보안 연결이 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21605-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="21605-111">예제</span><span class="sxs-lookup"><span data-stu-id="21605-111">EXAMPLES</span></span>

### <span data-ttu-id="21605-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="21605-112">Example 1</span></span>
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

<span data-ttu-id="21605-113">리소스 그룹 "myRG" 내에서 이름이 "myTunnel"인 Virtual Network 게이트웨이 연결에 대한 IKE 보안 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21605-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="21605-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21605-114">PARAMETERS</span></span>

### <span data-ttu-id="21605-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21605-115">-AsJob</span></span>
<span data-ttu-id="21605-116">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="21605-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="21605-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21605-117">-DefaultProfile</span></span>
<span data-ttu-id="21605-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21605-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21605-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21605-119">-InputObject</span></span>
<span data-ttu-id="21605-120">IKE SAS를 페치해야 하는 가상 네트워크 게이트웨이 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="21605-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="21605-121">-Name</span><span class="sxs-lookup"><span data-stu-id="21605-121">-Name</span></span>
<span data-ttu-id="21605-122">IKE SAS를 페치해야 하는 가상 네트워크 게이트웨이 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21605-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="21605-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21605-123">-ResourceGroupName</span></span>
<span data-ttu-id="21605-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21605-124">The resource group name.</span></span>

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

### <span data-ttu-id="21605-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21605-125">-ResourceId</span></span>
<span data-ttu-id="21605-126">IKE SAS를 페치해야 하는 Virtual Network 게이트웨이 연결의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="21605-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="21605-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21605-127">CommonParameters</span></span>
<span data-ttu-id="21605-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21605-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21605-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21605-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21605-130">입력</span><span class="sxs-lookup"><span data-stu-id="21605-130">INPUTS</span></span>

### <span data-ttu-id="21605-131">System.String</span><span class="sxs-lookup"><span data-stu-id="21605-131">System.String</span></span>

## <span data-ttu-id="21605-132">출력</span><span class="sxs-lookup"><span data-stu-id="21605-132">OUTPUTS</span></span>

### <span data-ttu-id="21605-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="21605-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="21605-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21605-134">NOTES</span></span>

## <span data-ttu-id="21605-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21605-135">RELATED LINKS</span></span>
