---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: af502cd4115ba9ef7467c15aa09b78e5e33c2337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998774"
---
# <span data-ttu-id="c739f-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="c739f-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="c739f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c739f-102">SYNOPSIS</span></span>
<span data-ttu-id="c739f-103">협회를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-103">Create or update an association.</span></span>

## <span data-ttu-id="c739f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c739f-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c739f-105">설명</span><span class="sxs-lookup"><span data-stu-id="c739f-105">DESCRIPTION</span></span>
<span data-ttu-id="c739f-106">협회를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-106">Create or update an association.</span></span>

## <span data-ttu-id="c739f-107">예제</span><span class="sxs-lookup"><span data-stu-id="c739f-107">EXAMPLES</span></span>

### <span data-ttu-id="c739f-108">예제 1: 사용자 지정 공급자 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="c739f-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="c739f-109">사용자 지정 공급자 연결 만들기, 연결된 대상 provioder는 "연결" 경로로 올바르게 구성되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="c739f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c739f-110">PARAMETERS</span></span>

### <span data-ttu-id="c739f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c739f-111">-AsJob</span></span>
<span data-ttu-id="c739f-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c739f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c739f-113">-DefaultProfile</span></span>
<span data-ttu-id="c739f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c739f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c739f-115">-Name</span></span>
<span data-ttu-id="c739f-116">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c739f-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c739f-117">-NoWait</span></span>
<span data-ttu-id="c739f-118">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="c739f-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c739f-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="c739f-119">-Scope</span></span>
<span data-ttu-id="c739f-120">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-120">The scope of the association.</span></span>
<span data-ttu-id="c739f-121">범위는 유효한 REST 리소스 인스턴스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="c739f-122">예를 들어 가상 머신 리소스에 대해 '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}'을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="c739f-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="c739f-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c739f-123">-TargetResourceId</span></span>
<span data-ttu-id="c739f-124">이 연결에 대한 대상 리소스의 REST 리소스 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="c739f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="c739f-125">-Confirm</span></span>
<span data-ttu-id="c739f-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c739f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c739f-127">-WhatIf</span></span>
<span data-ttu-id="c739f-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c739f-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c739f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c739f-130">CommonParameters</span></span>
<span data-ttu-id="c739f-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c739f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c739f-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c739f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c739f-133">입력</span><span class="sxs-lookup"><span data-stu-id="c739f-133">INPUTS</span></span>

## <span data-ttu-id="c739f-134">출력</span><span class="sxs-lookup"><span data-stu-id="c739f-134">OUTPUTS</span></span>

### <span data-ttu-id="c739f-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="c739f-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="c739f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c739f-136">NOTES</span></span>

<span data-ttu-id="c739f-137">별칭</span><span class="sxs-lookup"><span data-stu-id="c739f-137">ALIASES</span></span>

## <span data-ttu-id="c739f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c739f-138">RELATED LINKS</span></span>

