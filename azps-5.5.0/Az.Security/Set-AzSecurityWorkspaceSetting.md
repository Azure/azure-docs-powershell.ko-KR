---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: a02d2685987844db5f88fafaf12d0c9aed4a3234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201788"
---
# <span data-ttu-id="85dc8-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="85dc8-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="85dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="85dc8-103">구독에 대한 작업 영역 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="85dc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="85dc8-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85dc8-105">설명</span><span class="sxs-lookup"><span data-stu-id="85dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="85dc8-106">구독에 대한 작업 영역 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="85dc8-107">구성된 작업 영역은 이 구독 내 VM에 설치된 Azure Log Analytics 에이전트에서 수집한 보안 데이터를 보유합니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="85dc8-108">예제</span><span class="sxs-lookup"><span data-stu-id="85dc8-108">EXAMPLES</span></span>

### <span data-ttu-id="85dc8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="85dc8-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="85dc8-110">Azure Log Analytics 에이전트에서 수집한 모든 보안 데이터를 저장하는 "securityuserws" 작업 영역이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="85dc8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85dc8-111">PARAMETERS</span></span>

### <span data-ttu-id="85dc8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dc8-112">-DefaultProfile</span></span>
<span data-ttu-id="85dc8-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85dc8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="85dc8-114">-Name</span></span>
<span data-ttu-id="85dc8-115">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-115">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dc8-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="85dc8-116">-Scope</span></span>
<span data-ttu-id="85dc8-117">범위입니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-117">Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dc8-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="85dc8-118">-WorkspaceId</span></span>
<span data-ttu-id="85dc8-119">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-119">Workspace ID.</span></span>

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

### <span data-ttu-id="85dc8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85dc8-120">-Confirm</span></span>
<span data-ttu-id="85dc8-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dc8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85dc8-122">-WhatIf</span></span>
<span data-ttu-id="85dc8-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="85dc8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85dc8-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dc8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dc8-125">CommonParameters</span></span>
<span data-ttu-id="85dc8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85dc8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dc8-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85dc8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dc8-128">입력</span><span class="sxs-lookup"><span data-stu-id="85dc8-128">INPUTS</span></span>

### <span data-ttu-id="85dc8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="85dc8-129">System.String</span></span>

## <span data-ttu-id="85dc8-130">출력</span><span class="sxs-lookup"><span data-stu-id="85dc8-130">OUTPUTS</span></span>

### <span data-ttu-id="85dc8-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="85dc8-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="85dc8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85dc8-132">NOTES</span></span>

## <span data-ttu-id="85dc8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85dc8-133">RELATED LINKS</span></span>
