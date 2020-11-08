---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047644"
---
# <span data-ttu-id="12e9f-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="12e9f-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="12e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="12e9f-103">외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="12e9f-103">Get external security solution</span></span> 

## <span data-ttu-id="12e9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12e9f-104">SYNTAX</span></span>

### <span data-ttu-id="12e9f-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="12e9f-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e9f-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="12e9f-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e9f-107">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="12e9f-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12e9f-108">리소스</span><span class="sxs-lookup"><span data-stu-id="12e9f-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12e9f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="12e9f-109">DESCRIPTION</span></span>
<span data-ttu-id="12e9f-110">외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="12e9f-110">Get external security solution</span></span>

## <span data-ttu-id="12e9f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="12e9f-111">EXAMPLES</span></span>

### <span data-ttu-id="12e9f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="12e9f-112">Example 1</span></span>
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

<span data-ttu-id="12e9f-113">구독에서 모든 외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="12e9f-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="12e9f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="12e9f-114">Example 2</span></span>
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

<span data-ttu-id="12e9f-115">특정 외부 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="12e9f-115">Get a specific external security solution</span></span>

## <span data-ttu-id="12e9f-116">변수</span><span class="sxs-lookup"><span data-stu-id="12e9f-116">PARAMETERS</span></span>

### <span data-ttu-id="12e9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e9f-117">-DefaultProfile</span></span>
<span data-ttu-id="12e9f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e9f-119">-위치</span><span class="sxs-lookup"><span data-stu-id="12e9f-119">-Location</span></span>
<span data-ttu-id="12e9f-120">Location.</span><span class="sxs-lookup"><span data-stu-id="12e9f-120">Location.</span></span>

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

### <span data-ttu-id="12e9f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="12e9f-121">-Name</span></span>
<span data-ttu-id="12e9f-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9f-122">Resource name.</span></span>

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

### <span data-ttu-id="12e9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="12e9f-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9f-124">Resource group name.</span></span>

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

### <span data-ttu-id="12e9f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e9f-125">-ResourceId</span></span>
<span data-ttu-id="12e9f-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9f-126">Resource ID.</span></span>

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

### <span data-ttu-id="12e9f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e9f-127">CommonParameters</span></span>
<span data-ttu-id="12e9f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e9f-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12e9f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e9f-130">입력</span><span class="sxs-lookup"><span data-stu-id="12e9f-130">INPUTS</span></span>

### <span data-ttu-id="12e9f-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="12e9f-131">System.String</span></span>

## <span data-ttu-id="12e9f-132">출력</span><span class="sxs-lookup"><span data-stu-id="12e9f-132">OUTPUTS</span></span>

### <span data-ttu-id="12e9f-133">Microsoft. Azure. i. i m a 솔루션. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="12e9f-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="12e9f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="12e9f-134">NOTES</span></span>

## <span data-ttu-id="12e9f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12e9f-135">RELATED LINKS</span></span>
