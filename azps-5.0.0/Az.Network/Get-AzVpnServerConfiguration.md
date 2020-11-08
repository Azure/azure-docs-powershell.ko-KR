---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218123"
---
# <span data-ttu-id="157f2-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="157f2-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="157f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="157f2-102">SYNOPSIS</span></span>
<span data-ttu-id="157f2-103">사이트 연결을 위한 기존 VpnServerConfiguration를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="157f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="157f2-104">SYNTAX</span></span>

### <span data-ttu-id="157f2-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="157f2-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="157f2-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157f2-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="157f2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="157f2-107">DESCRIPTION</span></span>
<span data-ttu-id="157f2-108">**AzVpnServerConfiguration** cmdlet은 사이트 연결 지점의 기존 VpnServerConfiguration를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="157f2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="157f2-109">EXAMPLES</span></span>

### <span data-ttu-id="157f2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="157f2-110">Example 1</span></span>
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

<span data-ttu-id="157f2-111">위의 명령은 기존 VpnServerConfiguration를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="157f2-112">변수</span><span class="sxs-lookup"><span data-stu-id="157f2-112">PARAMETERS</span></span>

### <span data-ttu-id="157f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157f2-113">-DefaultProfile</span></span>
<span data-ttu-id="157f2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="157f2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="157f2-115">-Name</span></span>
<span data-ttu-id="157f2-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-116">The resource name.</span></span>

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

### <span data-ttu-id="157f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="157f2-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-118">The resource group name.</span></span>

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

### <span data-ttu-id="157f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157f2-119">CommonParameters</span></span>
<span data-ttu-id="157f2-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="157f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157f2-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157f2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157f2-122">입력</span><span class="sxs-lookup"><span data-stu-id="157f2-122">INPUTS</span></span>

### <span data-ttu-id="157f2-123">않아야</span><span class="sxs-lookup"><span data-stu-id="157f2-123">None</span></span>

## <span data-ttu-id="157f2-124">출력</span><span class="sxs-lookup"><span data-stu-id="157f2-124">OUTPUTS</span></span>

### <span data-ttu-id="157f2-125">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="157f2-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="157f2-126">상속자</span><span class="sxs-lookup"><span data-stu-id="157f2-126">NOTES</span></span>

## <span data-ttu-id="157f2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="157f2-127">RELATED LINKS</span></span>
