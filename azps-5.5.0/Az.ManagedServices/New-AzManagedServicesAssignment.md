---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187473"
---
# <span data-ttu-id="e5168-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="e5168-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="e5168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5168-102">SYNOPSIS</span></span>
<span data-ttu-id="e5168-103">등록 할당을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="e5168-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5168-104">SYNTAX</span></span>

### <span data-ttu-id="e5168-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5168-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5168-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5168-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5168-107">설명</span><span class="sxs-lookup"><span data-stu-id="e5168-107">DESCRIPTION</span></span>
<span data-ttu-id="e5168-108">등록 할당을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="e5168-109">예제</span><span class="sxs-lookup"><span data-stu-id="e5168-109">EXAMPLES</span></span>

### <span data-ttu-id="e5168-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5168-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="e5168-111">등록 정의 식별자를 사용하여 기본 범위에서 등록 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="e5168-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e5168-112">Example 2</span></span>
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


PS C:\>
```

<span data-ttu-id="e5168-113">등록 정의 개체를 입력으로 사용하여 등록 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="e5168-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="e5168-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="e5168-115">등록 정의 식별자 및 이름으로 등록 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="e5168-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5168-116">PARAMETERS</span></span>

### <span data-ttu-id="e5168-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5168-117">-DefaultProfile</span></span>
<span data-ttu-id="e5168-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5168-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e5168-119">-Name</span></span>
<span data-ttu-id="e5168-120">등록 할당의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="e5168-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e5168-121">-RegistrationDefinition</span></span>
<span data-ttu-id="e5168-122">등록 정의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-122">The registration definition input object.</span></span>

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

### <span data-ttu-id="e5168-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e5168-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="e5168-124">등록 정의의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5168-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="e5168-125">-Scope</span></span>
<span data-ttu-id="e5168-126">등록 할당을 만들어야 하는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="e5168-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5168-127">-AsJob</span></span>
<span data-ttu-id="e5168-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e5168-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5168-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5168-129">-Confirm</span></span>
<span data-ttu-id="e5168-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5168-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5168-131">-WhatIf</span></span>
<span data-ttu-id="e5168-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e5168-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5168-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5168-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5168-134">CommonParameters</span></span>
<span data-ttu-id="e5168-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5168-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5168-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5168-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5168-137">입력</span><span class="sxs-lookup"><span data-stu-id="e5168-137">INPUTS</span></span>

### <span data-ttu-id="e5168-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e5168-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="e5168-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e5168-139">System.String</span></span>
## <span data-ttu-id="e5168-140">출력</span><span class="sxs-lookup"><span data-stu-id="e5168-140">OUTPUTS</span></span>

### <span data-ttu-id="e5168-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="e5168-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="e5168-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5168-142">NOTES</span></span>

## <span data-ttu-id="e5168-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5168-143">RELATED LINKS</span></span>
