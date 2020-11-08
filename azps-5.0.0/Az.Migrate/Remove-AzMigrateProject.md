---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218628"
---
# <span data-ttu-id="f2eee-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="f2eee-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="f2eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2eee-102">SYNOPSIS</span></span>
<span data-ttu-id="f2eee-103">마이그레이션 프로젝트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-103">Delete the migrate project.</span></span>
<span data-ttu-id="f2eee-104">존재 하지 않는 프로젝트를 삭제 하는 것은 작업 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="f2eee-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f2eee-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2eee-106">설명은</span><span class="sxs-lookup"><span data-stu-id="f2eee-106">DESCRIPTION</span></span>
<span data-ttu-id="f2eee-107">마이그레이션 프로젝트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-107">Delete the migrate project.</span></span>
<span data-ttu-id="f2eee-108">존재 하지 않는 프로젝트를 삭제 하는 것은 작업 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="f2eee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f2eee-109">EXAMPLES</span></span>

### <span data-ttu-id="f2eee-110">예제 1: 삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2eee-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="f2eee-111">마이그레이션 프로젝트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-111">Delete the migrate project.</span></span>
<span data-ttu-id="f2eee-112">존재 하지 않는 프로젝트를 삭제 하는 것은 작업 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="f2eee-113">변수</span><span class="sxs-lookup"><span data-stu-id="f2eee-113">PARAMETERS</span></span>

### <span data-ttu-id="f2eee-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="f2eee-114">-AcceptLanguage</span></span>
<span data-ttu-id="f2eee-115">표준 요청 헤더.</span><span class="sxs-lookup"><span data-stu-id="f2eee-115">Standard request header.</span></span>
<span data-ttu-id="f2eee-116">서비스에서 해당 언어로 클라이언트에 응답 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="f2eee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2eee-117">-DefaultProfile</span></span>
<span data-ttu-id="f2eee-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2eee-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f2eee-119">-Name</span></span>
<span data-ttu-id="f2eee-120">Azure 마이그레이션 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="f2eee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2eee-121">-PassThru</span></span>
<span data-ttu-id="f2eee-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2eee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2eee-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2eee-124">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="f2eee-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2eee-125">-SubscriptionId</span></span>
<span data-ttu-id="f2eee-126">마이그레이션 프로젝트를 만든 Azure 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="f2eee-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f2eee-127">-Confirm</span></span>
<span data-ttu-id="f2eee-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2eee-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2eee-129">-WhatIf</span></span>
<span data-ttu-id="f2eee-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2eee-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2eee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2eee-132">CommonParameters</span></span>
<span data-ttu-id="f2eee-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2eee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2eee-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2eee-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2eee-135">입력</span><span class="sxs-lookup"><span data-stu-id="f2eee-135">INPUTS</span></span>

## <span data-ttu-id="f2eee-136">출력</span><span class="sxs-lookup"><span data-stu-id="f2eee-136">OUTPUTS</span></span>

### <span data-ttu-id="f2eee-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f2eee-137">System.Boolean</span></span>

## <span data-ttu-id="f2eee-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f2eee-138">NOTES</span></span>

<span data-ttu-id="f2eee-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="f2eee-139">ALIASES</span></span>

## <span data-ttu-id="f2eee-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2eee-140">RELATED LINKS</span></span>

