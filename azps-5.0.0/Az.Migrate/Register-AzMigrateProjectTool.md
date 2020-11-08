---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218633"
---
# <span data-ttu-id="f358e-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="f358e-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="f358e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f358e-102">SYNOPSIS</span></span>
<span data-ttu-id="f358e-103">마이그레이션 프로젝트에 도구를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="f358e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f358e-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f358e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f358e-105">DESCRIPTION</span></span>
<span data-ttu-id="f358e-106">마이그레이션 프로젝트에 도구를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="f358e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f358e-107">EXAMPLES</span></span>

### <span data-ttu-id="f358e-108">예제 1: 등록 도구</span><span class="sxs-lookup"><span data-stu-id="f358e-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="f358e-109">마이그레이션 프로젝트에 도구를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="f358e-110">변수</span><span class="sxs-lookup"><span data-stu-id="f358e-110">PARAMETERS</span></span>

### <span data-ttu-id="f358e-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="f358e-111">-AcceptLanguage</span></span>
<span data-ttu-id="f358e-112">표준 요청 헤더.</span><span class="sxs-lookup"><span data-stu-id="f358e-112">Standard request header.</span></span>
<span data-ttu-id="f358e-113">서비스에서 해당 언어로 클라이언트에 응답 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="f358e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f358e-114">-DefaultProfile</span></span>
<span data-ttu-id="f358e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f358e-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="f358e-116">-MigrateProjectName</span></span>
<span data-ttu-id="f358e-117">Azure 마이그레이션 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="f358e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f358e-118">-ResourceGroupName</span></span>
<span data-ttu-id="f358e-119">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="f358e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f358e-120">-SubscriptionId</span></span>
<span data-ttu-id="f358e-121">마이그레이션 프로젝트를 만든 Azure 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="f358e-122">-도구</span><span class="sxs-lookup"><span data-stu-id="f358e-122">-Tool</span></span>
<span data-ttu-id="f358e-123">등록할 도구를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="f358e-124">-확인</span><span class="sxs-lookup"><span data-stu-id="f358e-124">-Confirm</span></span>
<span data-ttu-id="f358e-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f358e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f358e-126">-WhatIf</span></span>
<span data-ttu-id="f358e-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f358e-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f358e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f358e-129">CommonParameters</span></span>
<span data-ttu-id="f358e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f358e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f358e-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f358e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f358e-132">입력</span><span class="sxs-lookup"><span data-stu-id="f358e-132">INPUTS</span></span>

## <span data-ttu-id="f358e-133">출력</span><span class="sxs-lookup"><span data-stu-id="f358e-133">OUTPUTS</span></span>

### <span data-ttu-id="f358e-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f358e-134">System.Boolean</span></span>

## <span data-ttu-id="f358e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="f358e-135">NOTES</span></span>

<span data-ttu-id="f358e-136">별칭과</span><span class="sxs-lookup"><span data-stu-id="f358e-136">ALIASES</span></span>

## <span data-ttu-id="f358e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f358e-137">RELATED LINKS</span></span>

