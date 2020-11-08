---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 5b905083668392ce026bfa416252eb1371ebb640
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041589"
---
# <span data-ttu-id="3bed4-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3bed4-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3bed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bed4-102">SYNOPSIS</span></span>
<span data-ttu-id="3bed4-103">구독에 구성 된 보안 작업 영역 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="3bed4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bed4-104">SYNTAX</span></span>

### <span data-ttu-id="3bed4-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3bed4-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bed4-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="3bed4-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bed4-107">리소스</span><span class="sxs-lookup"><span data-stu-id="3bed4-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bed4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3bed4-108">DESCRIPTION</span></span>
<span data-ttu-id="3bed4-109">이 cmdlet을 사용 하면이 구독 내의 Vm에 설치 된 보안 에이전트에서 수집한 보안 데이터를 저장할 구성 된 작업 영역을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="3bed4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3bed4-110">EXAMPLES</span></span>

### <span data-ttu-id="3bed4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bed4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="3bed4-112">구독에 대 한 작업 영역 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="3bed4-113">변수</span><span class="sxs-lookup"><span data-stu-id="3bed4-113">PARAMETERS</span></span>

### <span data-ttu-id="3bed4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bed4-114">-DefaultProfile</span></span>
<span data-ttu-id="3bed4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bed4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="3bed4-116">-Name</span></span>
<span data-ttu-id="3bed4-117">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-117">Resource name.</span></span>

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

### <span data-ttu-id="3bed4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bed4-118">-ResourceId</span></span>
<span data-ttu-id="3bed4-119">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-119">Resource ID.</span></span>

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

### <span data-ttu-id="3bed4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bed4-120">CommonParameters</span></span>
<span data-ttu-id="3bed4-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bed4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bed4-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bed4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bed4-123">입력</span><span class="sxs-lookup"><span data-stu-id="3bed4-123">INPUTS</span></span>

### <span data-ttu-id="3bed4-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3bed4-124">System.String</span></span>

## <span data-ttu-id="3bed4-125">출력</span><span class="sxs-lookup"><span data-stu-id="3bed4-125">OUTPUTS</span></span>

### <span data-ttu-id="3bed4-126">WorkspaceSettings. PSSecurityWorkspaceSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="3bed4-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3bed4-127">상속자</span><span class="sxs-lookup"><span data-stu-id="3bed4-127">NOTES</span></span>

## <span data-ttu-id="3bed4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bed4-128">RELATED LINKS</span></span>