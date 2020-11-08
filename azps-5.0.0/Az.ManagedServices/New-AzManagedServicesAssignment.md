---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217334"
---
# <span data-ttu-id="cefd1-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="cefd1-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="cefd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cefd1-102">SYNOPSIS</span></span>
<span data-ttu-id="cefd1-103">등록 과제를 작성 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="cefd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cefd1-104">SYNTAX</span></span>

### <span data-ttu-id="cefd1-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cefd1-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cefd1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cefd1-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cefd1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cefd1-107">DESCRIPTION</span></span>
<span data-ttu-id="cefd1-108">등록 과제를 작성 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="cefd1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cefd1-109">EXAMPLES</span></span>

### <span data-ttu-id="cefd1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cefd1-110">Example 1</span></span>
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

<span data-ttu-id="cefd1-111">등록 정의 식별자를 사용 하 여 기본 범위에서 등록 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="cefd1-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="cefd1-112">Example 2</span></span>
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

<span data-ttu-id="cefd1-113">등록 정의 개체를 입력으로 사용 하 여 등록 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="cefd1-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="cefd1-114">Example 3</span></span>
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

<span data-ttu-id="cefd1-115">등록 정의 식별자 및 이름을 사용 하 여 등록 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="cefd1-116">변수</span><span class="sxs-lookup"><span data-stu-id="cefd1-116">PARAMETERS</span></span>

### <span data-ttu-id="cefd1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefd1-117">-DefaultProfile</span></span>
<span data-ttu-id="cefd1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cefd1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="cefd1-119">-Name</span></span>
<span data-ttu-id="cefd1-120">등록 과제의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="cefd1-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="cefd1-121">-RegistrationDefinition</span></span>
<span data-ttu-id="cefd1-122">등록 정의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-122">The registration definition input object.</span></span>

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

### <span data-ttu-id="cefd1-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="cefd1-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="cefd1-124">정합 정의의 정규화 된 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-124">The fully qualified resource id of the registration definition.</span></span>

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

### <span data-ttu-id="cefd1-125">-범위</span><span class="sxs-lookup"><span data-stu-id="cefd1-125">-Scope</span></span>
<span data-ttu-id="cefd1-126">등록 과제를 만들어야 하는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="cefd1-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cefd1-127">-AsJob</span></span>
<span data-ttu-id="cefd1-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cefd1-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cefd1-129">-확인</span><span class="sxs-lookup"><span data-stu-id="cefd1-129">-Confirm</span></span>
<span data-ttu-id="cefd1-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cefd1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cefd1-131">-WhatIf</span></span>
<span data-ttu-id="cefd1-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cefd1-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cefd1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefd1-134">CommonParameters</span></span>
<span data-ttu-id="cefd1-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefd1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefd1-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cefd1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefd1-137">입력</span><span class="sxs-lookup"><span data-stu-id="cefd1-137">INPUTS</span></span>

### <span data-ttu-id="cefd1-138">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="cefd1-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="cefd1-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cefd1-139">System.String</span></span>
## <span data-ttu-id="cefd1-140">출력</span><span class="sxs-lookup"><span data-stu-id="cefd1-140">OUTPUTS</span></span>

### <span data-ttu-id="cefd1-141">Microsoft. PowerShell. a i m.</span><span class="sxs-lookup"><span data-stu-id="cefd1-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="cefd1-142">상속자</span><span class="sxs-lookup"><span data-stu-id="cefd1-142">NOTES</span></span>

## <span data-ttu-id="cefd1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cefd1-143">RELATED LINKS</span></span>
