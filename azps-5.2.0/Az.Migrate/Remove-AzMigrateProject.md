---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371015"
---
# <span data-ttu-id="9dc46-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="9dc46-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="9dc46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dc46-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc46-103">마이그레이션 프로젝트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-103">Delete the migrate project.</span></span>
<span data-ttu-id="9dc46-104">존재하지 않는 프로젝트를 삭제하는 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="9dc46-105">구문</span><span class="sxs-lookup"><span data-stu-id="9dc46-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9dc46-106">설명</span><span class="sxs-lookup"><span data-stu-id="9dc46-106">DESCRIPTION</span></span>
<span data-ttu-id="9dc46-107">마이그레이션 프로젝트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-107">Delete the migrate project.</span></span>
<span data-ttu-id="9dc46-108">존재하지 않는 프로젝트를 삭제하는 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="9dc46-109">예제</span><span class="sxs-lookup"><span data-stu-id="9dc46-109">EXAMPLES</span></span>

### <span data-ttu-id="9dc46-110">예제 1: 삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="9dc46-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="9dc46-111">마이그레이션 프로젝트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-111">Delete the migrate project.</span></span>
<span data-ttu-id="9dc46-112">존재하지 않는 프로젝트를 삭제하는 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="9dc46-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dc46-113">PARAMETERS</span></span>

### <span data-ttu-id="9dc46-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="9dc46-114">-AcceptLanguage</span></span>
<span data-ttu-id="9dc46-115">표준 요청 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-115">Standard request header.</span></span>
<span data-ttu-id="9dc46-116">서비스에서 적절한 언어로 클라이언트에 응답하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-116">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc46-117">-DefaultProfile</span></span>
<span data-ttu-id="9dc46-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc46-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9dc46-119">-Name</span></span>
<span data-ttu-id="9dc46-120">Azure Migrate 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc46-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc46-121">-PassThru</span></span>
<span data-ttu-id="9dc46-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9dc46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc46-123">-ResourceGroupName</span></span>
<span data-ttu-id="9dc46-124">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름은 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="9dc46-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9dc46-125">-SubscriptionId</span></span>
<span data-ttu-id="9dc46-126">마이그레이션 프로젝트를 만든 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-126">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc46-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dc46-127">-Confirm</span></span>
<span data-ttu-id="9dc46-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc46-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc46-129">-WhatIf</span></span>
<span data-ttu-id="9dc46-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9dc46-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc46-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc46-132">CommonParameters</span></span>
<span data-ttu-id="9dc46-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc46-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9dc46-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc46-135">입력</span><span class="sxs-lookup"><span data-stu-id="9dc46-135">INPUTS</span></span>

## <span data-ttu-id="9dc46-136">출력</span><span class="sxs-lookup"><span data-stu-id="9dc46-136">OUTPUTS</span></span>

### <span data-ttu-id="9dc46-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9dc46-137">System.Boolean</span></span>

## <span data-ttu-id="9dc46-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9dc46-138">NOTES</span></span>

<span data-ttu-id="9dc46-139">별칭</span><span class="sxs-lookup"><span data-stu-id="9dc46-139">ALIASES</span></span>

## <span data-ttu-id="9dc46-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9dc46-140">RELATED LINKS</span></span>

