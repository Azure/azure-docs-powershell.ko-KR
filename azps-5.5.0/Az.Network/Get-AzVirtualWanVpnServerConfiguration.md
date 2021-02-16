---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191937"
---
# <span data-ttu-id="60217-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="60217-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="60217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60217-102">SYNOPSIS</span></span>
<span data-ttu-id="60217-103">이 VirtualWan과 연결된 모든 VpnServerConfigurations 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60217-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="60217-104">구문</span><span class="sxs-lookup"><span data-stu-id="60217-104">SYNTAX</span></span>

### <span data-ttu-id="60217-105">ByVirtualWanName(기본값)</span><span class="sxs-lookup"><span data-stu-id="60217-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60217-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="60217-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60217-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="60217-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60217-108">설명</span><span class="sxs-lookup"><span data-stu-id="60217-108">DESCRIPTION</span></span>
<span data-ttu-id="60217-109">**Get-AzVirtualWanVpnServerConfiguration** cmdlet은 이 VirtualWan과 연결된 모든 VpnServerConfigurations 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="60217-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="60217-110">즉, 이 VirtualWan의 VirutalHubs 아래에 있는 모든 P2SVpnGateways에 연결된 모든 VpnServerConfigurations입니다.</span><span class="sxs-lookup"><span data-stu-id="60217-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="60217-111">예제</span><span class="sxs-lookup"><span data-stu-id="60217-111">EXAMPLES</span></span>

### <span data-ttu-id="60217-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="60217-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="60217-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60217-113">PARAMETERS</span></span>

### <span data-ttu-id="60217-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60217-114">-DefaultProfile</span></span>
<span data-ttu-id="60217-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60217-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60217-116">-Name</span><span class="sxs-lookup"><span data-stu-id="60217-116">-Name</span></span>
<span data-ttu-id="60217-117">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60217-117">The resource name.</span></span>

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

### <span data-ttu-id="60217-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60217-118">-ResourceGroupName</span></span>
<span data-ttu-id="60217-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60217-119">The resource group name.</span></span>

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

### <span data-ttu-id="60217-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60217-120">-ResourceId</span></span>
<span data-ttu-id="60217-121">가상 wan에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="60217-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="60217-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="60217-122">-VirtualWanObject</span></span>
<span data-ttu-id="60217-123">가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="60217-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="60217-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60217-124">CommonParameters</span></span>
<span data-ttu-id="60217-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60217-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60217-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="60217-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60217-127">입력</span><span class="sxs-lookup"><span data-stu-id="60217-127">INPUTS</span></span>

### <span data-ttu-id="60217-128">System.String</span><span class="sxs-lookup"><span data-stu-id="60217-128">System.String</span></span>
<span data-ttu-id="60217-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="60217-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="60217-130">출력</span><span class="sxs-lookup"><span data-stu-id="60217-130">OUTPUTS</span></span>

### <span data-ttu-id="60217-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="60217-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="60217-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60217-132">NOTES</span></span>

## <span data-ttu-id="60217-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60217-133">RELATED LINKS</span></span>
