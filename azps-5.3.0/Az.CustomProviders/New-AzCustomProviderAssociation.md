---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493623"
---
# <span data-ttu-id="1b23b-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="1b23b-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="1b23b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b23b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b23b-103">연결 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="1b23b-103">Create or update an association.</span></span>

## <span data-ttu-id="1b23b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b23b-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b23b-105">설명</span><span class="sxs-lookup"><span data-stu-id="1b23b-105">DESCRIPTION</span></span>
<span data-ttu-id="1b23b-106">연결 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="1b23b-106">Create or update an association.</span></span>

## <span data-ttu-id="1b23b-107">예제</span><span class="sxs-lookup"><span data-stu-id="1b23b-107">EXAMPLES</span></span>

### <span data-ttu-id="1b23b-108">예제 1: 사용자 지정 공급자 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="1b23b-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="1b23b-109">사용자 지정 공급자 연결 만들기, "연결"에 대한 경로로 연결된 대상 provioder를 올바르게 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="1b23b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b23b-110">PARAMETERS</span></span>

### <span data-ttu-id="1b23b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b23b-111">-AsJob</span></span>
<span data-ttu-id="1b23b-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1b23b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1b23b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b23b-113">-DefaultProfile</span></span>
<span data-ttu-id="1b23b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b23b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1b23b-115">-Name</span></span>
<span data-ttu-id="1b23b-116">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-116">The name of the association.</span></span>

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

### <span data-ttu-id="1b23b-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b23b-117">-NoWait</span></span>
<span data-ttu-id="1b23b-118">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1b23b-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b23b-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="1b23b-119">-Scope</span></span>
<span data-ttu-id="1b23b-120">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-120">The scope of the association.</span></span>
<span data-ttu-id="1b23b-121">범위는 유효한 REST 리소스 인스턴스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="1b23b-122">예를 들어 가상 머신 리소스에 '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}'을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="1b23b-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1b23b-123">-TargetResourceId</span></span>
<span data-ttu-id="1b23b-124">이 연결에 대한 대상 리소스의 REST 리소스 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="1b23b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b23b-125">-Confirm</span></span>
<span data-ttu-id="1b23b-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b23b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b23b-127">-WhatIf</span></span>
<span data-ttu-id="1b23b-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1b23b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b23b-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b23b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b23b-130">CommonParameters</span></span>
<span data-ttu-id="1b23b-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b23b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b23b-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b23b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b23b-133">입력</span><span class="sxs-lookup"><span data-stu-id="1b23b-133">INPUTS</span></span>

## <span data-ttu-id="1b23b-134">출력</span><span class="sxs-lookup"><span data-stu-id="1b23b-134">OUTPUTS</span></span>

### <span data-ttu-id="1b23b-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="1b23b-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="1b23b-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b23b-136">NOTES</span></span>

<span data-ttu-id="1b23b-137">별칭</span><span class="sxs-lookup"><span data-stu-id="1b23b-137">ALIASES</span></span>

## <span data-ttu-id="1b23b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b23b-138">RELATED LINKS</span></span>

