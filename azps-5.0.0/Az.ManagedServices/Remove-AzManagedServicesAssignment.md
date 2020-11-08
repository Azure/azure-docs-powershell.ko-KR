---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217333"
---
# <span data-ttu-id="c27a1-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="c27a1-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="c27a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c27a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c27a1-103">등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="c27a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c27a1-104">SYNTAX</span></span>

### <span data-ttu-id="c27a1-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c27a1-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c27a1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c27a1-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c27a1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c27a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c27a1-108">등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="c27a1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c27a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c27a1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c27a1-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="c27a1-111">기본 범위에서 이름으로 등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="c27a1-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c27a1-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="c27a1-113">제공 된 입력 개체를 사용 하 여 등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="c27a1-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="c27a1-114">Example 3</span></span>
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

<span data-ttu-id="c27a1-115">지정 된 범위에서 이름으로 등록 할당을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="c27a1-116">변수</span><span class="sxs-lookup"><span data-stu-id="c27a1-116">PARAMETERS</span></span>

### <span data-ttu-id="c27a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27a1-117">-DefaultProfile</span></span>
<span data-ttu-id="c27a1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c27a1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c27a1-119">-InputObject</span></span>
<span data-ttu-id="c27a1-120">등록 과제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-120">The registration assignment object.</span></span>

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

### <span data-ttu-id="c27a1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c27a1-121">-Name</span></span>
<span data-ttu-id="c27a1-122">등록 과제의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-122">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="c27a1-123">-범위</span><span class="sxs-lookup"><span data-stu-id="c27a1-123">-Scope</span></span>
<span data-ttu-id="c27a1-124">등록 과제의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-124">The scope of the registration assignment.</span></span>

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

### <span data-ttu-id="c27a1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c27a1-125">-AsJob</span></span>
<span data-ttu-id="c27a1-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c27a1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c27a1-127">-확인</span><span class="sxs-lookup"><span data-stu-id="c27a1-127">-Confirm</span></span>
<span data-ttu-id="c27a1-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c27a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c27a1-129">-WhatIf</span></span>
<span data-ttu-id="c27a1-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c27a1-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c27a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27a1-132">CommonParameters</span></span>
<span data-ttu-id="c27a1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c27a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27a1-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c27a1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27a1-135">입력</span><span class="sxs-lookup"><span data-stu-id="c27a1-135">INPUTS</span></span>

### <span data-ttu-id="c27a1-136">Microsoft. PowerShell. a i m.</span><span class="sxs-lookup"><span data-stu-id="c27a1-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="c27a1-137">출력</span><span class="sxs-lookup"><span data-stu-id="c27a1-137">OUTPUTS</span></span>

### <span data-ttu-id="c27a1-138">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c27a1-138">System.Void</span></span>
## <span data-ttu-id="c27a1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c27a1-139">NOTES</span></span>

## <span data-ttu-id="c27a1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c27a1-140">RELATED LINKS</span></span>
