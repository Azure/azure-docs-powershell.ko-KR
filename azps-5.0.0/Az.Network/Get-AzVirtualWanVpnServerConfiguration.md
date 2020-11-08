---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216895"
---
# <span data-ttu-id="69430-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="69430-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="69430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69430-102">SYNOPSIS</span></span>
<span data-ttu-id="69430-103">이 VirtualWan과 연결 된 모든 VpnServerConfigurations 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69430-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="69430-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69430-104">SYNTAX</span></span>

### <span data-ttu-id="69430-105">ByVirtualWanName (기본값)</span><span class="sxs-lookup"><span data-stu-id="69430-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69430-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="69430-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69430-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="69430-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69430-108">설명은</span><span class="sxs-lookup"><span data-stu-id="69430-108">DESCRIPTION</span></span>
<span data-ttu-id="69430-109">**AzVirtualWanVpnServerConfiguration** cmdlet은이 virtualwan과 연결 된 모든 VpnServerConfigurations 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69430-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="69430-110">즉,이 VirtualWan의 VirutalHubs 아래에 있는 모든 P2SVpnGateways에 연결 된 모든 VpnServerConfigurations.</span><span class="sxs-lookup"><span data-stu-id="69430-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="69430-111">예제의</span><span class="sxs-lookup"><span data-stu-id="69430-111">EXAMPLES</span></span>

### <span data-ttu-id="69430-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="69430-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="69430-113">변수</span><span class="sxs-lookup"><span data-stu-id="69430-113">PARAMETERS</span></span>

### <span data-ttu-id="69430-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69430-114">-DefaultProfile</span></span>
<span data-ttu-id="69430-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69430-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69430-116">-이름</span><span class="sxs-lookup"><span data-stu-id="69430-116">-Name</span></span>
<span data-ttu-id="69430-117">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69430-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69430-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69430-118">-ResourceGroupName</span></span>
<span data-ttu-id="69430-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69430-119">The resource group name.</span></span>

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

### <span data-ttu-id="69430-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69430-120">-ResourceId</span></span>
<span data-ttu-id="69430-121">가상 wan에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69430-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69430-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="69430-122">-VirtualWanObject</span></span>
<span data-ttu-id="69430-123">가상 wan 개체.</span><span class="sxs-lookup"><span data-stu-id="69430-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69430-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69430-124">CommonParameters</span></span>
<span data-ttu-id="69430-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69430-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69430-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69430-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69430-127">입력</span><span class="sxs-lookup"><span data-stu-id="69430-127">INPUTS</span></span>

### <span data-ttu-id="69430-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69430-128">System.String</span></span>
<span data-ttu-id="69430-129">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="69430-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="69430-130">출력</span><span class="sxs-lookup"><span data-stu-id="69430-130">OUTPUTS</span></span>

### <span data-ttu-id="69430-131">PSVpnServerConfigurationsResponse에 대 한.</span><span class="sxs-lookup"><span data-stu-id="69430-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="69430-132">상속자</span><span class="sxs-lookup"><span data-stu-id="69430-132">NOTES</span></span>

## <span data-ttu-id="69430-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69430-133">RELATED LINKS</span></span>
