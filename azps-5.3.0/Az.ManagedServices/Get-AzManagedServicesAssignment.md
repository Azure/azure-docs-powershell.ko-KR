---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491937"
---
# <span data-ttu-id="25a88-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="25a88-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="25a88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a88-102">SYNOPSIS</span></span>
<span data-ttu-id="25a88-103">특정 등록 할당 또는 등록 할당 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="25a88-104">구문</span><span class="sxs-lookup"><span data-stu-id="25a88-104">SYNTAX</span></span>

### <span data-ttu-id="25a88-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="25a88-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a88-106">ByName</span><span class="sxs-lookup"><span data-stu-id="25a88-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25a88-107">설명</span><span class="sxs-lookup"><span data-stu-id="25a88-107">DESCRIPTION</span></span>
<span data-ttu-id="25a88-108">특정 등록 할당 또는 등록 할당 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="25a88-109">예제</span><span class="sxs-lookup"><span data-stu-id="25a88-109">EXAMPLES</span></span>

### <span data-ttu-id="25a88-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="25a88-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="25a88-111">기본 범위에서 모든 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="25a88-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="25a88-112">Example 2</span></span>
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

<span data-ttu-id="25a88-113">등록 정의 세부 정보가 있는 모든 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="25a88-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="25a88-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="25a88-115">등록 정의 세부 정보 없이 이름으로 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="25a88-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="25a88-116">Example 4</span></span>
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

<span data-ttu-id="25a88-117">등록 정의 세부 정보가 있는 이름으로 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="25a88-118">예제 5</span><span class="sxs-lookup"><span data-stu-id="25a88-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="25a88-119">주어진 범위에서 모든 등록 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="25a88-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25a88-120">PARAMETERS</span></span>

### <span data-ttu-id="25a88-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a88-121">-DefaultProfile</span></span>
<span data-ttu-id="25a88-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a88-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="25a88-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="25a88-124">등록 정의 세부 정보를 포함할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="25a88-125">-Name</span><span class="sxs-lookup"><span data-stu-id="25a88-125">-Name</span></span>
<span data-ttu-id="25a88-126">등록 할당의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="25a88-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="25a88-127">-Scope</span></span>
<span data-ttu-id="25a88-128">등록 할당이 만들어진 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="25a88-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a88-129">CommonParameters</span></span>
<span data-ttu-id="25a88-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25a88-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a88-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25a88-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a88-132">입력</span><span class="sxs-lookup"><span data-stu-id="25a88-132">INPUTS</span></span>

### <span data-ttu-id="25a88-133">없음</span><span class="sxs-lookup"><span data-stu-id="25a88-133">None</span></span>
## <span data-ttu-id="25a88-134">출력</span><span class="sxs-lookup"><span data-stu-id="25a88-134">OUTPUTS</span></span>

### <span data-ttu-id="25a88-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="25a88-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="25a88-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25a88-136">NOTES</span></span>

## <span data-ttu-id="25a88-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25a88-137">RELATED LINKS</span></span>
