---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379632"
---
# <span data-ttu-id="3c57a-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c57a-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="3c57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c57a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c57a-103">지점 및 사이트 연결에 대한 기존 VpnServerConfiguration을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="3c57a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c57a-104">SYNTAX</span></span>

### <span data-ttu-id="3c57a-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c57a-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c57a-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c57a-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c57a-107">설명</span><span class="sxs-lookup"><span data-stu-id="3c57a-107">DESCRIPTION</span></span>
<span data-ttu-id="3c57a-108">**Get-AzVpnServerConfiguration** cmdlet은 지점 및 사이트 연결에 대한 기존 VpnServerConfiguration을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="3c57a-109">예제</span><span class="sxs-lookup"><span data-stu-id="3c57a-109">EXAMPLES</span></span>

### <span data-ttu-id="3c57a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c57a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="3c57a-111">위의 명령은 기존 VpnServerConfiguration을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="3c57a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c57a-112">PARAMETERS</span></span>

### <span data-ttu-id="3c57a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c57a-113">-DefaultProfile</span></span>
<span data-ttu-id="3c57a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c57a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3c57a-115">-Name</span></span>
<span data-ttu-id="3c57a-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c57a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c57a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c57a-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c57a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c57a-119">CommonParameters</span></span>
<span data-ttu-id="3c57a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c57a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c57a-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3c57a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c57a-122">입력</span><span class="sxs-lookup"><span data-stu-id="3c57a-122">INPUTS</span></span>

### <span data-ttu-id="3c57a-123">없음</span><span class="sxs-lookup"><span data-stu-id="3c57a-123">None</span></span>

## <span data-ttu-id="3c57a-124">출력</span><span class="sxs-lookup"><span data-stu-id="3c57a-124">OUTPUTS</span></span>

### <span data-ttu-id="3c57a-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c57a-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="3c57a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c57a-126">NOTES</span></span>

## <span data-ttu-id="3c57a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c57a-127">RELATED LINKS</span></span>
