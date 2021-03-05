---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: b351cfaa5d94c7104972158dc9dee6363a7d466b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984080"
---
# <span data-ttu-id="efa18-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="efa18-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="efa18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa18-102">SYNOPSIS</span></span>
<span data-ttu-id="efa18-103">이 구독에 대한 보안 작업 영역 설정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="efa18-104">구문</span><span class="sxs-lookup"><span data-stu-id="efa18-104">SYNTAX</span></span>

### <span data-ttu-id="efa18-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="efa18-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa18-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="efa18-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa18-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="efa18-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa18-108">설명</span><span class="sxs-lookup"><span data-stu-id="efa18-108">DESCRIPTION</span></span>
<span data-ttu-id="efa18-109">이 구독에 대한 보안 작업 영역 설정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="efa18-110">이 작업은 새로 설치된 보안 에이전트가 이 구독의 기본 작업 영역으로 보고할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="efa18-111">예제</span><span class="sxs-lookup"><span data-stu-id="efa18-111">EXAMPLES</span></span>

### <span data-ttu-id="efa18-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="efa18-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="efa18-113">이 구독에 대한 보안 작업 영역 설정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="efa18-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="efa18-114">PARAMETERS</span></span>

### <span data-ttu-id="efa18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa18-115">-DefaultProfile</span></span>
<span data-ttu-id="efa18-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa18-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa18-117">-InputObject</span></span>
<span data-ttu-id="efa18-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-118">Input Object.</span></span>

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

### <span data-ttu-id="efa18-119">-Name</span><span class="sxs-lookup"><span data-stu-id="efa18-119">-Name</span></span>
<span data-ttu-id="efa18-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-120">Resource name.</span></span>

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

### <span data-ttu-id="efa18-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efa18-121">-PassThru</span></span>
<span data-ttu-id="efa18-122">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="efa18-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efa18-123">-ResourceId</span></span>
<span data-ttu-id="efa18-124">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-124">Resource ID.</span></span>

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

### <span data-ttu-id="efa18-125">-확인</span><span class="sxs-lookup"><span data-stu-id="efa18-125">-Confirm</span></span>
<span data-ttu-id="efa18-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa18-127">-WhatIf</span></span>
<span data-ttu-id="efa18-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efa18-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa18-130">CommonParameters</span></span>
<span data-ttu-id="efa18-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efa18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa18-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa18-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa18-133">입력</span><span class="sxs-lookup"><span data-stu-id="efa18-133">INPUTS</span></span>

### <span data-ttu-id="efa18-134">System.String</span><span class="sxs-lookup"><span data-stu-id="efa18-134">System.String</span></span>

### <span data-ttu-id="efa18-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="efa18-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="efa18-136">출력</span><span class="sxs-lookup"><span data-stu-id="efa18-136">OUTPUTS</span></span>

### <span data-ttu-id="efa18-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efa18-137">System.Boolean</span></span>

## <span data-ttu-id="efa18-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efa18-138">NOTES</span></span>

## <span data-ttu-id="efa18-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efa18-139">RELATED LINKS</span></span>
