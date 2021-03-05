---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: f0de174ac85fb4247ac8af55f8a8ab9cb64d6446
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973504"
---
# <span data-ttu-id="80a9b-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="80a9b-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="80a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="80a9b-103">구독에서 구성된 보안 작업 영역 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="80a9b-104">구문</span><span class="sxs-lookup"><span data-stu-id="80a9b-104">SYNTAX</span></span>

### <span data-ttu-id="80a9b-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="80a9b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a9b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="80a9b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a9b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a9b-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80a9b-108">설명</span><span class="sxs-lookup"><span data-stu-id="80a9b-108">DESCRIPTION</span></span>
<span data-ttu-id="80a9b-109">이 cmdlet을 사용하면 이 구독 내에서 VM에 설치된 보안 에이전트에서 수집한 보안 데이터를 보유하는 구성된 작업 영역이 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="80a9b-110">예제</span><span class="sxs-lookup"><span data-stu-id="80a9b-110">EXAMPLES</span></span>

### <span data-ttu-id="80a9b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="80a9b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="80a9b-112">구독에 대한 작업 영역 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="80a9b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="80a9b-113">PARAMETERS</span></span>

### <span data-ttu-id="80a9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a9b-114">-DefaultProfile</span></span>
<span data-ttu-id="80a9b-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a9b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="80a9b-116">-Name</span></span>
<span data-ttu-id="80a9b-117">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a9b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a9b-118">-ResourceId</span></span>
<span data-ttu-id="80a9b-119">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-119">Resource ID.</span></span>

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

### <span data-ttu-id="80a9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a9b-120">CommonParameters</span></span>
<span data-ttu-id="80a9b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80a9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a9b-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80a9b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a9b-123">입력</span><span class="sxs-lookup"><span data-stu-id="80a9b-123">INPUTS</span></span>

### <span data-ttu-id="80a9b-124">System.String</span><span class="sxs-lookup"><span data-stu-id="80a9b-124">System.String</span></span>

## <span data-ttu-id="80a9b-125">출력</span><span class="sxs-lookup"><span data-stu-id="80a9b-125">OUTPUTS</span></span>

### <span data-ttu-id="80a9b-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="80a9b-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="80a9b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80a9b-127">NOTES</span></span>

## <span data-ttu-id="80a9b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80a9b-128">RELATED LINKS</span></span>
