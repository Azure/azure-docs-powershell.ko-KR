---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 79780c101296d78115a1c88ef4d4aebcd3721c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041583"
---
# <span data-ttu-id="b2619-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b2619-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b2619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2619-102">SYNOPSIS</span></span>
<span data-ttu-id="b2619-103">이 구독에 대 한 보안 작업 영역 설정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="b2619-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2619-104">SYNTAX</span></span>

### <span data-ttu-id="b2619-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2619-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2619-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b2619-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2619-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2619-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2619-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b2619-108">DESCRIPTION</span></span>
<span data-ttu-id="b2619-109">이 구독에 대 한 보안 작업 영역 설정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="b2619-110">이 작업을 수행 하면 새로 설치 된 보안 에이전트가이 구독의 기본 작업 영역으로 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="b2619-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b2619-111">EXAMPLES</span></span>

### <span data-ttu-id="b2619-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2619-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="b2619-113">이 구독에 대 한 보안 작업 영역 설정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="b2619-114">변수</span><span class="sxs-lookup"><span data-stu-id="b2619-114">PARAMETERS</span></span>

### <span data-ttu-id="b2619-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2619-115">-DefaultProfile</span></span>
<span data-ttu-id="b2619-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2619-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2619-117">-InputObject</span></span>
<span data-ttu-id="b2619-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="b2619-118">Input Object.</span></span>

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

### <span data-ttu-id="b2619-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b2619-119">-Name</span></span>
<span data-ttu-id="b2619-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-120">Resource name.</span></span>

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

### <span data-ttu-id="b2619-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2619-121">-PassThru</span></span>
<span data-ttu-id="b2619-122">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b2619-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2619-123">-ResourceId</span></span>
<span data-ttu-id="b2619-124">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-124">Resource ID.</span></span>

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

### <span data-ttu-id="b2619-125">-확인</span><span class="sxs-lookup"><span data-stu-id="b2619-125">-Confirm</span></span>
<span data-ttu-id="b2619-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2619-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2619-127">-WhatIf</span></span>
<span data-ttu-id="b2619-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2619-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2619-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2619-130">CommonParameters</span></span>
<span data-ttu-id="b2619-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2619-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2619-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2619-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2619-133">입력</span><span class="sxs-lookup"><span data-stu-id="b2619-133">INPUTS</span></span>

### <span data-ttu-id="b2619-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2619-134">System.String</span></span>

### <span data-ttu-id="b2619-135">WorkspaceSettings. PSSecurityWorkspaceSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="b2619-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b2619-136">출력</span><span class="sxs-lookup"><span data-stu-id="b2619-136">OUTPUTS</span></span>

### <span data-ttu-id="b2619-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b2619-137">System.Boolean</span></span>

## <span data-ttu-id="b2619-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b2619-138">NOTES</span></span>

## <span data-ttu-id="b2619-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2619-139">RELATED LINKS</span></span>
