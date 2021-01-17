---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337466"
---
# <span data-ttu-id="85150-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="85150-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="85150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85150-102">SYNOPSIS</span></span>
<span data-ttu-id="85150-103">외부 보안 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="85150-103">Get external security solution</span></span> 

## <span data-ttu-id="85150-104">구문</span><span class="sxs-lookup"><span data-stu-id="85150-104">SYNTAX</span></span>

### <span data-ttu-id="85150-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="85150-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85150-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="85150-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85150-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="85150-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85150-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="85150-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85150-109">설명</span><span class="sxs-lookup"><span data-stu-id="85150-109">DESCRIPTION</span></span>
<span data-ttu-id="85150-110">외부 보안 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="85150-110">Get external security solution</span></span>

## <span data-ttu-id="85150-111">예제</span><span class="sxs-lookup"><span data-stu-id="85150-111">EXAMPLES</span></span>

### <span data-ttu-id="85150-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="85150-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="85150-113">구독의 모든 외부 보안 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="85150-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="85150-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="85150-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="85150-115">특정 외부 보안 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="85150-115">Get a specific external security solution</span></span>

## <span data-ttu-id="85150-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85150-116">PARAMETERS</span></span>

### <span data-ttu-id="85150-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85150-117">-DefaultProfile</span></span>
<span data-ttu-id="85150-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85150-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85150-119">-Location</span><span class="sxs-lookup"><span data-stu-id="85150-119">-Location</span></span>
<span data-ttu-id="85150-120">위치.</span><span class="sxs-lookup"><span data-stu-id="85150-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85150-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85150-121">-Name</span></span>
<span data-ttu-id="85150-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85150-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85150-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85150-123">-ResourceGroupName</span></span>
<span data-ttu-id="85150-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85150-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85150-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85150-125">-ResourceId</span></span>
<span data-ttu-id="85150-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85150-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85150-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85150-127">CommonParameters</span></span>
<span data-ttu-id="85150-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85150-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85150-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85150-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85150-130">입력</span><span class="sxs-lookup"><span data-stu-id="85150-130">INPUTS</span></span>

### <span data-ttu-id="85150-131">System.String</span><span class="sxs-lookup"><span data-stu-id="85150-131">System.String</span></span>

## <span data-ttu-id="85150-132">출력</span><span class="sxs-lookup"><span data-stu-id="85150-132">OUTPUTS</span></span>

### <span data-ttu-id="85150-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="85150-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="85150-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85150-134">NOTES</span></span>

## <span data-ttu-id="85150-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85150-135">RELATED LINKS</span></span>
