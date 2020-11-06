---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531947"
---
# <span data-ttu-id="d652f-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="d652f-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d652f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d652f-102">SYNOPSIS</span></span>
<span data-ttu-id="d652f-103">구독에 대 한 작업 영역 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d652f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d652f-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d652f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d652f-105">DESCRIPTION</span></span>
<span data-ttu-id="d652f-106">구독에 대 한 작업 영역 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="d652f-107">구성 된 작업 영역에는이 구독 내의 Vm에 설치 되어 있는 보안 에이전트에서 수집한 보안 데이터가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="d652f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d652f-108">EXAMPLES</span></span>

### <span data-ttu-id="d652f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d652f-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="d652f-110">"MyWorkspace" 작업 영역에 보안 에이전트가 수집한 모든 보안 데이터를 저장 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="d652f-111">변수</span><span class="sxs-lookup"><span data-stu-id="d652f-111">PARAMETERS</span></span>

### <span data-ttu-id="d652f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d652f-112">-DefaultProfile</span></span>
<span data-ttu-id="d652f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="d652f-114">-Name</span></span>
<span data-ttu-id="d652f-115">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652f-116">-범위</span><span class="sxs-lookup"><span data-stu-id="d652f-116">-Scope</span></span>
<span data-ttu-id="d652f-117">범위도.</span><span class="sxs-lookup"><span data-stu-id="d652f-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652f-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d652f-118">-WorkspaceId</span></span>
<span data-ttu-id="d652f-119">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d652f-120">-확인</span><span class="sxs-lookup"><span data-stu-id="d652f-120">-Confirm</span></span>
<span data-ttu-id="d652f-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d652f-122">-WhatIf</span></span>
<span data-ttu-id="d652f-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d652f-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d652f-125">CommonParameters</span></span>
<span data-ttu-id="d652f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d652f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d652f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d652f-128">입력</span><span class="sxs-lookup"><span data-stu-id="d652f-128">INPUTS</span></span>

### <span data-ttu-id="d652f-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d652f-129">System.String</span></span>

## <span data-ttu-id="d652f-130">출력</span><span class="sxs-lookup"><span data-stu-id="d652f-130">OUTPUTS</span></span>

### <span data-ttu-id="d652f-131">WorkspaceSettings. PSSecurityWorkspaceSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d652f-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d652f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d652f-132">NOTES</span></span>

## <span data-ttu-id="d652f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d652f-133">RELATED LINKS</span></span>
