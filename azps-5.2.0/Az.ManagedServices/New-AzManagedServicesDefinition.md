---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368222"
---
# <span data-ttu-id="a8b1a-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a8b1a-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="a8b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b1a-103">등록 정의를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="a8b1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8b1a-104">SYNTAX</span></span>

### <span data-ttu-id="a8b1a-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="a8b1a-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b1a-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="a8b1a-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8b1a-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="a8b1a-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b1a-108">설명</span><span class="sxs-lookup"><span data-stu-id="a8b1a-108">DESCRIPTION</span></span>
<span data-ttu-id="a8b1a-109">등록 정의를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="a8b1a-110">예제</span><span class="sxs-lookup"><span data-stu-id="a8b1a-110">EXAMPLES</span></span>

### <span data-ttu-id="a8b1a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8b1a-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="a8b1a-112">roleDefinitionId 및 principalId 값을 직접 통해 등록 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="a8b1a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a8b1a-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="a8b1a-114">권한 부여 세부 정보를 통해 등록 정의를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="a8b1a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="a8b1a-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="a8b1a-116">등록 정의를 권한 부여 세부 정보 및 등록 정의의 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="a8b1a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8b1a-117">PARAMETERS</span></span>

### <span data-ttu-id="a8b1a-118">-Authorization</span><span class="sxs-lookup"><span data-stu-id="a8b1a-118">-Authorization</span></span>
<span data-ttu-id="a8b1a-119">principalId - roleDefinitionId를 사용하는 권한 부여 매핑 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b1a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b1a-120">-DefaultProfile</span></span>
<span data-ttu-id="a8b1a-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8b1a-122">-Description</span><span class="sxs-lookup"><span data-stu-id="a8b1a-122">-Description</span></span>
<span data-ttu-id="a8b1a-123">등록 정의에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-123">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="a8b1a-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8b1a-124">-DisplayName</span></span>
<span data-ttu-id="a8b1a-125">등록 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-125">The display name of the Registration Definition.</span></span>

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

### <span data-ttu-id="a8b1a-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="a8b1a-126">-ManagedByTenantId</span></span>
<span data-ttu-id="a8b1a-127">ManagedBy 테넌트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-127">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="a8b1a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a8b1a-128">-Name</span></span>
<span data-ttu-id="a8b1a-129">등록 정의의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-129">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="a8b1a-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a8b1a-130">-PlanName</span></span>
<span data-ttu-id="a8b1a-131">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b1a-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="a8b1a-132">-PlanProduct</span></span>
<span data-ttu-id="a8b1a-133">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b1a-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="a8b1a-134">-PlanPublisher</span></span>
<span data-ttu-id="a8b1a-135">Publisher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b1a-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="a8b1a-136">-PlanVersion</span></span>
<span data-ttu-id="a8b1a-137">계획의 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b1a-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="a8b1a-138">-PrincipalId</span></span>
<span data-ttu-id="a8b1a-139">ManagedBy 보안 주체 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-139">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="a8b1a-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a8b1a-140">-RoleDefinitionId</span></span>
<span data-ttu-id="a8b1a-141">보안 주체 식별자에 권한을 부여할 역할 정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-141">The role definition identifier to grant permissions to principal identifier.</span></span>

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

### <span data-ttu-id="a8b1a-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8b1a-142">-AsJob</span></span>
<span data-ttu-id="a8b1a-143">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a8b1a-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8b1a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8b1a-144">-Confirm</span></span>
<span data-ttu-id="a8b1a-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b1a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b1a-146">-WhatIf</span></span>
<span data-ttu-id="a8b1a-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a8b1a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8b1a-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b1a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b1a-149">CommonParameters</span></span>
<span data-ttu-id="a8b1a-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b1a-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b1a-152">입력</span><span class="sxs-lookup"><span data-stu-id="a8b1a-152">INPUTS</span></span>

### <span data-ttu-id="a8b1a-153">없음</span><span class="sxs-lookup"><span data-stu-id="a8b1a-153">None</span></span>
## <span data-ttu-id="a8b1a-154">출력</span><span class="sxs-lookup"><span data-stu-id="a8b1a-154">OUTPUTS</span></span>

### <span data-ttu-id="a8b1a-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="a8b1a-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="a8b1a-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8b1a-156">NOTES</span></span>

## <span data-ttu-id="a8b1a-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8b1a-157">RELATED LINKS</span></span>
