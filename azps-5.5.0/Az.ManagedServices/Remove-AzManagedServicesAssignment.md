---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180313"
---
# <span data-ttu-id="fc5cd-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="fc5cd-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="fc5cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5cd-103">등록 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="fc5cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc5cd-104">SYNTAX</span></span>

### <span data-ttu-id="fc5cd-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5cd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc5cd-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5cd-107">설명</span><span class="sxs-lookup"><span data-stu-id="fc5cd-107">DESCRIPTION</span></span>
<span data-ttu-id="fc5cd-108">등록 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="fc5cd-109">예제</span><span class="sxs-lookup"><span data-stu-id="fc5cd-109">EXAMPLES</span></span>

### <span data-ttu-id="fc5cd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc5cd-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="fc5cd-111">기본 범위에서 이름으로 등록 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="fc5cd-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fc5cd-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="fc5cd-113">제공된 입력 개체를 사용하여 등록 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="fc5cd-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="fc5cd-114">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="fc5cd-115">지정한 범위에서 이름으로 등록 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="fc5cd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc5cd-116">PARAMETERS</span></span>

### <span data-ttu-id="fc5cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5cd-117">-DefaultProfile</span></span>
<span data-ttu-id="fc5cd-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5cd-119">-InputObject</span></span>
<span data-ttu-id="fc5cd-120">등록 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fc5cd-121">-Name</span></span>
<span data-ttu-id="fc5cd-122">등록 할당의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-122">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="fc5cd-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="fc5cd-123">-Scope</span></span>
<span data-ttu-id="fc5cd-124">등록 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-124">The scope of the registration assignment.</span></span>

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

### <span data-ttu-id="fc5cd-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc5cd-125">-AsJob</span></span>
<span data-ttu-id="fc5cd-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fc5cd-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc5cd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc5cd-127">-Confirm</span></span>
<span data-ttu-id="fc5cd-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5cd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5cd-129">-WhatIf</span></span>
<span data-ttu-id="fc5cd-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fc5cd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5cd-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5cd-132">CommonParameters</span></span>
<span data-ttu-id="fc5cd-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5cd-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5cd-135">입력</span><span class="sxs-lookup"><span data-stu-id="fc5cd-135">INPUTS</span></span>

### <span data-ttu-id="fc5cd-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="fc5cd-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="fc5cd-137">출력</span><span class="sxs-lookup"><span data-stu-id="fc5cd-137">OUTPUTS</span></span>

### <span data-ttu-id="fc5cd-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="fc5cd-138">System.Void</span></span>
## <span data-ttu-id="fc5cd-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc5cd-139">NOTES</span></span>

## <span data-ttu-id="fc5cd-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc5cd-140">RELATED LINKS</span></span>
