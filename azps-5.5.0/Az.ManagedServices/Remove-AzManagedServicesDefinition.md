---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187460"
---
# <span data-ttu-id="1def5-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1def5-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="1def5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1def5-102">SYNOPSIS</span></span>
<span data-ttu-id="1def5-103">등록 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="1def5-104">구문</span><span class="sxs-lookup"><span data-stu-id="1def5-104">SYNTAX</span></span>

### <span data-ttu-id="1def5-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="1def5-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1def5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1def5-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1def5-107">설명</span><span class="sxs-lookup"><span data-stu-id="1def5-107">DESCRIPTION</span></span>
<span data-ttu-id="1def5-108">등록 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="1def5-109">예제</span><span class="sxs-lookup"><span data-stu-id="1def5-109">EXAMPLES</span></span>

### <span data-ttu-id="1def5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1def5-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="1def5-111">기본 범위에서 이름으로 등록 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="1def5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1def5-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="1def5-113">입력 개체가 제공된 등록 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="1def5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1def5-114">PARAMETERS</span></span>

### <span data-ttu-id="1def5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1def5-115">-DefaultProfile</span></span>
<span data-ttu-id="1def5-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1def5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1def5-117">-InputObject</span></span>
<span data-ttu-id="1def5-118">등록 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1def5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1def5-119">-Name</span></span>
<span data-ttu-id="1def5-120">등록 정의의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1def5-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="1def5-121">-Scope</span></span>
<span data-ttu-id="1def5-122">등록 정의를 만든 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1def5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1def5-123">-Confirm</span></span>
<span data-ttu-id="1def5-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1def5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1def5-125">-WhatIf</span></span>
<span data-ttu-id="1def5-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1def5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1def5-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1def5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1def5-128">CommonParameters</span></span>
<span data-ttu-id="1def5-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1def5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1def5-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1def5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1def5-131">입력</span><span class="sxs-lookup"><span data-stu-id="1def5-131">INPUTS</span></span>

### <span data-ttu-id="1def5-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1def5-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="1def5-133">출력</span><span class="sxs-lookup"><span data-stu-id="1def5-133">OUTPUTS</span></span>

### <span data-ttu-id="1def5-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="1def5-134">System.Void</span></span>
## <span data-ttu-id="1def5-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1def5-135">NOTES</span></span>

## <span data-ttu-id="1def5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1def5-136">RELATED LINKS</span></span>
