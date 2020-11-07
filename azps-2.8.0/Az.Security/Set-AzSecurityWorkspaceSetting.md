---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: c425a7d11fab8bc019ca3944d034dfa2bfb96d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873174"
---
# <span data-ttu-id="32c84-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="32c84-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="32c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32c84-102">SYNOPSIS</span></span>
<span data-ttu-id="32c84-103">구독에 대 한 작업 영역 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="32c84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32c84-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32c84-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32c84-105">DESCRIPTION</span></span>
<span data-ttu-id="32c84-106">구독에 대 한 작업 영역 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="32c84-107">구성 된 작업 영역에는이 구독 내의 Vm에 설치 되어 있는 Azure 로그 분석 에이전트 에이전트에서 수집한 보안 데이터가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="32c84-108">예제의</span><span class="sxs-lookup"><span data-stu-id="32c84-108">EXAMPLES</span></span>

### <span data-ttu-id="32c84-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="32c84-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="32c84-110">"MyWorkspace" 작업 영역을 설정 하 여 Azure 로그 분석 에이전트에서 수집한 모든 보안 데이터를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="32c84-111">변수</span><span class="sxs-lookup"><span data-stu-id="32c84-111">PARAMETERS</span></span>

### <span data-ttu-id="32c84-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c84-112">-DefaultProfile</span></span>
<span data-ttu-id="32c84-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32c84-114">-이름</span><span class="sxs-lookup"><span data-stu-id="32c84-114">-Name</span></span>
<span data-ttu-id="32c84-115">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-115">Resource name.</span></span>

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

### <span data-ttu-id="32c84-116">-범위</span><span class="sxs-lookup"><span data-stu-id="32c84-116">-Scope</span></span>
<span data-ttu-id="32c84-117">범위도.</span><span class="sxs-lookup"><span data-stu-id="32c84-117">Scope.</span></span>

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

### <span data-ttu-id="32c84-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="32c84-118">-WorkspaceId</span></span>
<span data-ttu-id="32c84-119">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-119">Workspace ID.</span></span>

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

### <span data-ttu-id="32c84-120">-확인</span><span class="sxs-lookup"><span data-stu-id="32c84-120">-Confirm</span></span>
<span data-ttu-id="32c84-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c84-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c84-122">-WhatIf</span></span>
<span data-ttu-id="32c84-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32c84-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c84-125">CommonParameters</span></span>
<span data-ttu-id="32c84-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c84-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32c84-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c84-128">입력</span><span class="sxs-lookup"><span data-stu-id="32c84-128">INPUTS</span></span>

### <span data-ttu-id="32c84-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32c84-129">System.String</span></span>

## <span data-ttu-id="32c84-130">출력</span><span class="sxs-lookup"><span data-stu-id="32c84-130">OUTPUTS</span></span>

### <span data-ttu-id="32c84-131">WorkspaceSettings. PSSecurityWorkspaceSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="32c84-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="32c84-132">상속자</span><span class="sxs-lookup"><span data-stu-id="32c84-132">NOTES</span></span>

## <span data-ttu-id="32c84-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32c84-133">RELATED LINKS</span></span>
