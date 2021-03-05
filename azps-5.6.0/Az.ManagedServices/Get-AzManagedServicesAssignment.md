---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f0398981f6c3a59c9401df4ec89208a5f8196b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965787"
---
# <span data-ttu-id="c3c82-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="c3c82-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="c3c82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3c82-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c82-103">특정 등록 할당 또는 등록 할당 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="c3c82-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3c82-104">SYNTAX</span></span>

### <span data-ttu-id="c3c82-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="c3c82-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3c82-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c3c82-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c82-107">설명</span><span class="sxs-lookup"><span data-stu-id="c3c82-107">DESCRIPTION</span></span>
<span data-ttu-id="c3c82-108">특정 등록 할당 또는 등록 할당 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="c3c82-109">예제</span><span class="sxs-lookup"><span data-stu-id="c3c82-109">EXAMPLES</span></span>

### <span data-ttu-id="c3c82-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3c82-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="c3c82-111">기본 범위에서 모든 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="c3c82-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3c82-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="c3c82-113">등록 정의 세부 정보를 통해 모든 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="c3c82-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="c3c82-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="c3c82-115">등록 정의 세부 정보가 없는 이름으로 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="c3c82-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="c3c82-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="c3c82-117">등록 정의 세부 정보가 있는 이름으로 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="c3c82-118">예제 5</span><span class="sxs-lookup"><span data-stu-id="c3c82-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="c3c82-119">주어진 범위에서 모든 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="c3c82-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c3c82-120">PARAMETERS</span></span>

### <span data-ttu-id="c3c82-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c82-121">-DefaultProfile</span></span>
<span data-ttu-id="c3c82-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c82-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="c3c82-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="c3c82-124">등록 정의 세부 정보를 포함할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c82-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c3c82-125">-Name</span></span>
<span data-ttu-id="c3c82-126">등록 할당의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c82-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="c3c82-127">-Scope</span></span>
<span data-ttu-id="c3c82-128">등록 할당이 만든 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="c3c82-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c82-129">CommonParameters</span></span>
<span data-ttu-id="c3c82-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3c82-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c82-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3c82-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c82-132">입력</span><span class="sxs-lookup"><span data-stu-id="c3c82-132">INPUTS</span></span>

### <span data-ttu-id="c3c82-133">없음</span><span class="sxs-lookup"><span data-stu-id="c3c82-133">None</span></span>
## <span data-ttu-id="c3c82-134">출력</span><span class="sxs-lookup"><span data-stu-id="c3c82-134">OUTPUTS</span></span>

### <span data-ttu-id="c3c82-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="c3c82-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="c3c82-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3c82-136">NOTES</span></span>

## <span data-ttu-id="c3c82-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3c82-137">RELATED LINKS</span></span>
