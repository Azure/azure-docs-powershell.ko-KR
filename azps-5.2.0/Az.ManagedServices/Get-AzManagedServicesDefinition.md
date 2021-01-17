---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323504"
---
# <span data-ttu-id="d04c9-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d04c9-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="d04c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d04c9-103">특정 등록 정의 또는 등록 정의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="d04c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="d04c9-104">SYNTAX</span></span>

### <span data-ttu-id="d04c9-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d04c9-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d04c9-106">기본값</span><span class="sxs-lookup"><span data-stu-id="d04c9-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d04c9-107">설명</span><span class="sxs-lookup"><span data-stu-id="d04c9-107">DESCRIPTION</span></span>
<span data-ttu-id="d04c9-108">특정 등록 정의 또는 등록 정의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="d04c9-109">예제</span><span class="sxs-lookup"><span data-stu-id="d04c9-109">EXAMPLES</span></span>

### <span data-ttu-id="d04c9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d04c9-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="d04c9-111">기본 범위에서 모든 등록 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="d04c9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d04c9-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="d04c9-113">기본 범위에서 이름으로 등록 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="d04c9-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="d04c9-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="d04c9-115">주어진 범위에서 모든 등록 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="d04c9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d04c9-116">PARAMETERS</span></span>

### <span data-ttu-id="d04c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04c9-117">-DefaultProfile</span></span>
<span data-ttu-id="d04c9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04c9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d04c9-119">-Name</span></span>
<span data-ttu-id="d04c9-120">등록 정의의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="d04c9-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="d04c9-121">-Scope</span></span>
<span data-ttu-id="d04c9-122">등록 정의를 만든 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="d04c9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04c9-123">CommonParameters</span></span>
<span data-ttu-id="d04c9-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d04c9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04c9-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d04c9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04c9-126">입력</span><span class="sxs-lookup"><span data-stu-id="d04c9-126">INPUTS</span></span>

### <span data-ttu-id="d04c9-127">없음</span><span class="sxs-lookup"><span data-stu-id="d04c9-127">None</span></span>
## <span data-ttu-id="d04c9-128">출력</span><span class="sxs-lookup"><span data-stu-id="d04c9-128">OUTPUTS</span></span>

### <span data-ttu-id="d04c9-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="d04c9-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="d04c9-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d04c9-130">NOTES</span></span>

## <span data-ttu-id="d04c9-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d04c9-131">RELATED LINKS</span></span>
