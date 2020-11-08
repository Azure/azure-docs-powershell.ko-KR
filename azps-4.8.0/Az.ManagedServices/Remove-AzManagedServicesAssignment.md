---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f2328ba75a0142a61238665eef41e32bf1fbba6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213524"
---
# <span data-ttu-id="f1d81-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f1d81-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="f1d81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d81-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d81-103">등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="f1d81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1d81-104">SYNTAX</span></span>

### <span data-ttu-id="f1d81-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1d81-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d81-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1d81-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d81-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f1d81-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d81-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f1d81-108">DESCRIPTION</span></span>
<span data-ttu-id="f1d81-109">등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="f1d81-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f1d81-110">EXAMPLES</span></span>

### <span data-ttu-id="f1d81-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1d81-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="f1d81-112">기본 범위에서 등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="f1d81-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f1d81-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="f1d81-114">정규화 된 리소스 id에 해당 하는 등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="f1d81-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f1d81-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="f1d81-116">제공 된 입력 개체를 사용 하 여 등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="f1d81-117">변수</span><span class="sxs-lookup"><span data-stu-id="f1d81-117">PARAMETERS</span></span>

### <span data-ttu-id="f1d81-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1d81-118">-AsJob</span></span>
<span data-ttu-id="f1d81-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f1d81-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1d81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d81-120">-DefaultProfile</span></span>
<span data-ttu-id="f1d81-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1d81-122">-Id</span><span class="sxs-lookup"><span data-stu-id="f1d81-122">-Id</span></span>
<span data-ttu-id="f1d81-123">등록 과제 GUID (예: b0c052e5-c437-4771-a476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="f1d81-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="f1d81-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1d81-124">-InputObject</span></span>
<span data-ttu-id="f1d81-125">등록 과제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-125">The registration assignment object.</span></span>

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

### <span data-ttu-id="f1d81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1d81-126">-ResourceId</span></span>
<span data-ttu-id="f1d81-127">등록 배정의 정규화 된 리소스 id (예:/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57)입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

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

### <span data-ttu-id="f1d81-128">-범위</span><span class="sxs-lookup"><span data-stu-id="f1d81-128">-Scope</span></span>
<span data-ttu-id="f1d81-129">등록 과제를 만들어야 하는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d81-130">-확인</span><span class="sxs-lookup"><span data-stu-id="f1d81-130">-Confirm</span></span>
<span data-ttu-id="f1d81-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d81-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d81-132">-WhatIf</span></span>
<span data-ttu-id="f1d81-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d81-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d81-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d81-135">CommonParameters</span></span>
<span data-ttu-id="f1d81-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d81-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d81-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1d81-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d81-138">입력</span><span class="sxs-lookup"><span data-stu-id="f1d81-138">INPUTS</span></span>

### <span data-ttu-id="f1d81-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1d81-139">System.String</span></span>

### <span data-ttu-id="f1d81-140">Microsoft. PowerShell. a i m.</span><span class="sxs-lookup"><span data-stu-id="f1d81-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="f1d81-141">출력</span><span class="sxs-lookup"><span data-stu-id="f1d81-141">OUTPUTS</span></span>

### <span data-ttu-id="f1d81-142">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="f1d81-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="f1d81-143">상속자</span><span class="sxs-lookup"><span data-stu-id="f1d81-143">NOTES</span></span>

## <span data-ttu-id="f1d81-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1d81-144">RELATED LINKS</span></span>
