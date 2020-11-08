---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 6c9c4b562acbf80dba9b1b414345d5eb8e3ecc60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044197"
---
# <span data-ttu-id="49947-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="49947-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="49947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49947-102">SYNOPSIS</span></span>
<span data-ttu-id="49947-103">등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49947-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="49947-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49947-104">SYNTAX</span></span>

### <span data-ttu-id="49947-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="49947-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49947-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="49947-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49947-107">설명은</span><span class="sxs-lookup"><span data-stu-id="49947-107">DESCRIPTION</span></span>
<span data-ttu-id="49947-108">등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49947-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="49947-109">예제의</span><span class="sxs-lookup"><span data-stu-id="49947-109">EXAMPLES</span></span>

### <span data-ttu-id="49947-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="49947-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="49947-111">필수 매개 변수를 지정 하 여 등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49947-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="49947-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="49947-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="49947-113">계획 세부 정보를 사용 하 여 등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49947-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="49947-114">변수</span><span class="sxs-lookup"><span data-stu-id="49947-114">PARAMETERS</span></span>

### <span data-ttu-id="49947-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49947-115">-AsJob</span></span>
<span data-ttu-id="49947-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="49947-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49947-117">-DefaultProfile</span></span>
<span data-ttu-id="49947-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49947-119">-설명</span><span class="sxs-lookup"><span data-stu-id="49947-119">-Description</span></span>
<span data-ttu-id="49947-120">등록 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="49947-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="49947-121">-ManagedByTenantId</span></span>
<span data-ttu-id="49947-122">ManagedBy 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-122">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="49947-123">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="49947-123">-PlanName</span></span>
<span data-ttu-id="49947-124">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-124">The name of the plan.</span></span>

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

### <span data-ttu-id="49947-125">계획 제품</span><span class="sxs-lookup"><span data-stu-id="49947-125">-PlanProduct</span></span>
<span data-ttu-id="49947-126">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-126">The name of the Product.</span></span>

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

### <span data-ttu-id="49947-127">-계획 Publisher</span><span class="sxs-lookup"><span data-stu-id="49947-127">-PlanPublisher</span></span>
<span data-ttu-id="49947-128">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-128">The name of the Publisher.</span></span>

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

### <span data-ttu-id="49947-129">-계획 버전</span><span class="sxs-lookup"><span data-stu-id="49947-129">-PlanVersion</span></span>
<span data-ttu-id="49947-130">계획의 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-130">The version number of the plan.</span></span>

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

### <span data-ttu-id="49947-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="49947-131">-PrincipalId</span></span>
<span data-ttu-id="49947-132">ManagedBy Principal 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-132">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="49947-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="49947-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="49947-134">등록 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-134">The name of the Registration Definition.</span></span>

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

### <span data-ttu-id="49947-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="49947-135">-RoleDefinitionId</span></span>
<span data-ttu-id="49947-136">관리 되는 서비스 공급자의 역할 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="49947-136">The Managed Service Provider's Role Identifier.</span></span>

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

### <span data-ttu-id="49947-137">-확인</span><span class="sxs-lookup"><span data-stu-id="49947-137">-Confirm</span></span>
<span data-ttu-id="49947-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49947-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49947-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49947-139">-WhatIf</span></span>
<span data-ttu-id="49947-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49947-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49947-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49947-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49947-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49947-142">CommonParameters</span></span>
<span data-ttu-id="49947-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49947-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49947-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49947-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49947-145">입력</span><span class="sxs-lookup"><span data-stu-id="49947-145">INPUTS</span></span>

### <span data-ttu-id="49947-146">않아야</span><span class="sxs-lookup"><span data-stu-id="49947-146">None</span></span>

## <span data-ttu-id="49947-147">출력</span><span class="sxs-lookup"><span data-stu-id="49947-147">OUTPUTS</span></span>

### <span data-ttu-id="49947-148">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="49947-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="49947-149">상속자</span><span class="sxs-lookup"><span data-stu-id="49947-149">NOTES</span></span>

## <span data-ttu-id="49947-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49947-150">RELATED LINKS</span></span>
