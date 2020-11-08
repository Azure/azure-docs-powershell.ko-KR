---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: c53489e943b2e8afc10f655b59c6ed076974198a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213532"
---
# <span data-ttu-id="eea77-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="eea77-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="eea77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea77-102">SYNOPSIS</span></span>
<span data-ttu-id="eea77-103">등록 과제를 작성 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="eea77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eea77-104">SYNTAX</span></span>

### <span data-ttu-id="eea77-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="eea77-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinitionName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea77-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eea77-106">ByResourceId</span></span>
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea77-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eea77-107">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinition <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea77-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eea77-108">DESCRIPTION</span></span>
<span data-ttu-id="eea77-109">등록 과제를 작성 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-109">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="eea77-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eea77-110">EXAMPLES</span></span>

### <span data-ttu-id="eea77-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="eea77-111">Example 1</span></span>
```powershell
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/d4d14a4c-9b54-4dc3-b755-6d0659e0224b

Name                                 RegistrationDefinitionId
----                                 ------------------------
3b3d5411-ec8c-4a52-8972-73f4952724b2 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/d4d14a4c-9b54-4dc3-b755-6d0659e0224b
```

<span data-ttu-id="eea77-112">등록 정의의 정규화 된 리소스 id가 지정 된 새 등록 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-112">Creates a new registration assignment given the fully qualified resource id of the registration definition.</span></span>

### <span data-ttu-id="eea77-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="eea77-113">Example 2</span></span>
```powershell
New-AzManagedServicesAssignment -Scope /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/resourceGroups/mygroup1 -RegistrationDefinitionName 47f471b3-ff5f-463c-8a1f-286501b01ddc

Name                                 RegistrationDefinitionId
----                                 ------------------------
5aa0d921-64b8-40e8-af33-31993f0deaa8 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/47f471b3-ff5f-463c-8a1f-286501b01ddc
```

<span data-ttu-id="eea77-114">지정 된 범위와 등록 정의 이름으로 등록 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-114">Creates a the registration assignment given a scope and the registration definition name.</span></span>

### <span data-ttu-id="eea77-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="eea77-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $def

Name                                 RegistrationDefinitionId
----                                 ------------------------
a25f63d9-605c-4878-99bd-0d315480d46b /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/4a50f8eb-96b3-44c4-a397-e1e57035fe65
```
<span data-ttu-id="eea77-116">등록 정의 개체가 제공 하는 등록 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-116">Creates a the registration assignment given a registration definition object.</span></span>
## <span data-ttu-id="eea77-117">변수</span><span class="sxs-lookup"><span data-stu-id="eea77-117">PARAMETERS</span></span>

### <span data-ttu-id="eea77-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eea77-118">-AsJob</span></span>
<span data-ttu-id="eea77-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eea77-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eea77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea77-120">-DefaultProfile</span></span>
<span data-ttu-id="eea77-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea77-122">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="eea77-122">-RegistrationDefinition</span></span>
<span data-ttu-id="eea77-123">등록 정의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-123">The registration definition input object.</span></span>

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

### <span data-ttu-id="eea77-124">-RegistrationDefinitionResourceId</span><span class="sxs-lookup"><span data-stu-id="eea77-124">-RegistrationDefinitionResourceId</span></span>
<span data-ttu-id="eea77-125">등록 정의의 정규화 된 리소스 id (예:/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)입니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-125">The fully qualified resource id of the registration definition (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eea77-126">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="eea77-126">-RegistrationDefinitionName</span></span>
<span data-ttu-id="eea77-127">등록 정의 이름입니다 (예: b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="eea77-127">The registration definition name (for example, b0c052e5-c437-4771-a476-8b1201158a57.</span></span>

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

### <span data-ttu-id="eea77-128">-범위</span><span class="sxs-lookup"><span data-stu-id="eea77-128">-Scope</span></span>
<span data-ttu-id="eea77-129">등록 과제를 만들어야 하는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea77-130">-확인</span><span class="sxs-lookup"><span data-stu-id="eea77-130">-Confirm</span></span>
<span data-ttu-id="eea77-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea77-132">-WhatIf</span></span>
<span data-ttu-id="eea77-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea77-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea77-135">CommonParameters</span></span>
<span data-ttu-id="eea77-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea77-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eea77-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea77-138">입력</span><span class="sxs-lookup"><span data-stu-id="eea77-138">INPUTS</span></span>

### <span data-ttu-id="eea77-139">않아야</span><span class="sxs-lookup"><span data-stu-id="eea77-139">None</span></span>

## <span data-ttu-id="eea77-140">출력</span><span class="sxs-lookup"><span data-stu-id="eea77-140">OUTPUTS</span></span>

### <span data-ttu-id="eea77-141">Microsoft. PowerShell. a i m.</span><span class="sxs-lookup"><span data-stu-id="eea77-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="eea77-142">상속자</span><span class="sxs-lookup"><span data-stu-id="eea77-142">NOTES</span></span>

## <span data-ttu-id="eea77-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eea77-143">RELATED LINKS</span></span>
