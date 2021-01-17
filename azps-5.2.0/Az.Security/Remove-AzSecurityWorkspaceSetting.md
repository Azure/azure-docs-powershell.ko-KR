---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339873"
---
# <span data-ttu-id="2384f-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="2384f-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="2384f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2384f-102">SYNOPSIS</span></span>
<span data-ttu-id="2384f-103">이 구독에 대한 보안 작업 영역 설정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="2384f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2384f-104">SYNTAX</span></span>

### <span data-ttu-id="2384f-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="2384f-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2384f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2384f-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2384f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2384f-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2384f-108">설명</span><span class="sxs-lookup"><span data-stu-id="2384f-108">DESCRIPTION</span></span>
<span data-ttu-id="2384f-109">이 구독에 대한 보안 작업 영역 설정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="2384f-110">이 작업을 수행하면 새로 설치된 보안 에이전트가 이 구독의 기본 작업 영역으로 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="2384f-111">예제</span><span class="sxs-lookup"><span data-stu-id="2384f-111">EXAMPLES</span></span>

### <span data-ttu-id="2384f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2384f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="2384f-113">이 구독에 대한 보안 작업 영역 설정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="2384f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2384f-114">PARAMETERS</span></span>

### <span data-ttu-id="2384f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2384f-115">-DefaultProfile</span></span>
<span data-ttu-id="2384f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2384f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2384f-117">-InputObject</span></span>
<span data-ttu-id="2384f-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2384f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2384f-119">-Name</span></span>
<span data-ttu-id="2384f-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-120">Resource name.</span></span>

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

### <span data-ttu-id="2384f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2384f-121">-PassThru</span></span>
<span data-ttu-id="2384f-122">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-122">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2384f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2384f-123">-ResourceId</span></span>
<span data-ttu-id="2384f-124">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-124">Resource ID.</span></span>

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

### <span data-ttu-id="2384f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2384f-125">-Confirm</span></span>
<span data-ttu-id="2384f-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2384f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2384f-127">-WhatIf</span></span>
<span data-ttu-id="2384f-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2384f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2384f-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2384f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2384f-130">CommonParameters</span></span>
<span data-ttu-id="2384f-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2384f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2384f-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2384f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2384f-133">입력</span><span class="sxs-lookup"><span data-stu-id="2384f-133">INPUTS</span></span>

### <span data-ttu-id="2384f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2384f-134">System.String</span></span>

### <span data-ttu-id="2384f-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="2384f-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="2384f-136">출력</span><span class="sxs-lookup"><span data-stu-id="2384f-136">OUTPUTS</span></span>

### <span data-ttu-id="2384f-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2384f-137">System.Boolean</span></span>

## <span data-ttu-id="2384f-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2384f-138">NOTES</span></span>

## <span data-ttu-id="2384f-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2384f-139">RELATED LINKS</span></span>
