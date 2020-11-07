---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 9d63c208daffe6e06da759ff929de120cab58c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689393"
---
# <span data-ttu-id="fb7bb-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="fb7bb-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="fb7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7bb-103">등록 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="fb7bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb7bb-104">SYNTAX</span></span>

### <span data-ttu-id="fb7bb-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb7bb-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7bb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7bb-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7bb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb7bb-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fb7bb-108">DESCRIPTION</span></span>
<span data-ttu-id="fb7bb-109">등록 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="fb7bb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fb7bb-110">EXAMPLES</span></span>

### <span data-ttu-id="fb7bb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb7bb-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="fb7bb-112">지정 된 등록 정의에 대 한 식별자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="fb7bb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fb7bb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="fb7bb-114">정규화 된 리소스 id 인 경우 등록 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="fb7bb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="fb7bb-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="fb7bb-116">개체가 제공 하는 등록 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="fb7bb-117">변수</span><span class="sxs-lookup"><span data-stu-id="fb7bb-117">PARAMETERS</span></span>

### <span data-ttu-id="fb7bb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb7bb-118">-AsJob</span></span>
<span data-ttu-id="fb7bb-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb7bb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb7bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7bb-120">-DefaultProfile</span></span>
<span data-ttu-id="fb7bb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7bb-122">-Id</span><span class="sxs-lookup"><span data-stu-id="fb7bb-122">-Id</span></span>
<span data-ttu-id="fb7bb-123">등록 정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="fb7bb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb7bb-124">-InputObject</span></span>
<span data-ttu-id="fb7bb-125">등록 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-125">The registration definition object.</span></span>

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

### <span data-ttu-id="fb7bb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7bb-126">-ResourceId</span></span>
<span data-ttu-id="fb7bb-127">등록 정의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7bb-127">ResourceId of the registration definition</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7bb-128">-확인</span><span class="sxs-lookup"><span data-stu-id="fb7bb-128">-Confirm</span></span>
<span data-ttu-id="fb7bb-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7bb-130">-WhatIf</span></span>
<span data-ttu-id="fb7bb-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7bb-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7bb-133">CommonParameters</span></span>
<span data-ttu-id="fb7bb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7bb-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7bb-136">입력</span><span class="sxs-lookup"><span data-stu-id="fb7bb-136">INPUTS</span></span>

### <span data-ttu-id="fb7bb-137">않아야</span><span class="sxs-lookup"><span data-stu-id="fb7bb-137">None</span></span>

## <span data-ttu-id="fb7bb-138">출력</span><span class="sxs-lookup"><span data-stu-id="fb7bb-138">OUTPUTS</span></span>

### <span data-ttu-id="fb7bb-139">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="fb7bb-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="fb7bb-140">상속자</span><span class="sxs-lookup"><span data-stu-id="fb7bb-140">NOTES</span></span>

## <span data-ttu-id="fb7bb-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb7bb-141">RELATED LINKS</span></span>
