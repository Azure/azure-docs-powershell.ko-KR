---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: cf06d1cce2e37f69ce06576a659dbfa989ca56b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871694"
---
# <span data-ttu-id="8527a-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8527a-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="8527a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8527a-102">SYNOPSIS</span></span>
<span data-ttu-id="8527a-103">외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="8527a-103">Get external security solution</span></span> 

## <span data-ttu-id="8527a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8527a-104">SYNTAX</span></span>

### <span data-ttu-id="8527a-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8527a-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8527a-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="8527a-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8527a-107">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="8527a-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8527a-108">리소스</span><span class="sxs-lookup"><span data-stu-id="8527a-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8527a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8527a-109">DESCRIPTION</span></span>
<span data-ttu-id="8527a-110">외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="8527a-110">Get external security solution</span></span>

## <span data-ttu-id="8527a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8527a-111">EXAMPLES</span></span>

### <span data-ttu-id="8527a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8527a-112">Example 1</span></span>
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

<span data-ttu-id="8527a-113">구독에서 모든 외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="8527a-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="8527a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8527a-114">Example 2</span></span>
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

<span data-ttu-id="8527a-115">특정 외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="8527a-115">Get a specific external security solution</span></span>

## <span data-ttu-id="8527a-116">변수</span><span class="sxs-lookup"><span data-stu-id="8527a-116">PARAMETERS</span></span>

### <span data-ttu-id="8527a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8527a-117">-DefaultProfile</span></span>
<span data-ttu-id="8527a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8527a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8527a-119">-위치</span><span class="sxs-lookup"><span data-stu-id="8527a-119">-Location</span></span>
<span data-ttu-id="8527a-120">Location.</span><span class="sxs-lookup"><span data-stu-id="8527a-120">Location.</span></span>

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

### <span data-ttu-id="8527a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8527a-121">-Name</span></span>
<span data-ttu-id="8527a-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8527a-122">Resource name.</span></span>

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

### <span data-ttu-id="8527a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8527a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8527a-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8527a-124">Resource group name.</span></span>

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

### <span data-ttu-id="8527a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8527a-125">-ResourceId</span></span>
<span data-ttu-id="8527a-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8527a-126">Resource ID.</span></span>

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

### <span data-ttu-id="8527a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8527a-127">CommonParameters</span></span>
<span data-ttu-id="8527a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8527a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8527a-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8527a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8527a-130">입력</span><span class="sxs-lookup"><span data-stu-id="8527a-130">INPUTS</span></span>

### <span data-ttu-id="8527a-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8527a-131">System.String</span></span>

## <span data-ttu-id="8527a-132">출력</span><span class="sxs-lookup"><span data-stu-id="8527a-132">OUTPUTS</span></span>

### <span data-ttu-id="8527a-133">Microsoft. Azure. i. i m a 솔루션. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8527a-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="8527a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="8527a-134">NOTES</span></span>

## <span data-ttu-id="8527a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8527a-135">RELATED LINKS</span></span>
