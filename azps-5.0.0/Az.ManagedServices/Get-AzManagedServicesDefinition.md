---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217336"
---
# <span data-ttu-id="b444d-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="b444d-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="b444d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b444d-102">SYNOPSIS</span></span>
<span data-ttu-id="b444d-103">특정 등록 정의 또는 등록 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="b444d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b444d-104">SYNTAX</span></span>

### <span data-ttu-id="b444d-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b444d-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b444d-106">기본값</span><span class="sxs-lookup"><span data-stu-id="b444d-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b444d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b444d-107">DESCRIPTION</span></span>
<span data-ttu-id="b444d-108">특정 등록 정의 또는 등록 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="b444d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b444d-109">EXAMPLES</span></span>

### <span data-ttu-id="b444d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b444d-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="b444d-111">기본 범위에서 모든 등록 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="b444d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b444d-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="b444d-113">기본 범위에서 이름으로 등록 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="b444d-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="b444d-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="b444d-115">지정 된 범위에 있는 모든 등록 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="b444d-116">변수</span><span class="sxs-lookup"><span data-stu-id="b444d-116">PARAMETERS</span></span>

### <span data-ttu-id="b444d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b444d-117">-DefaultProfile</span></span>
<span data-ttu-id="b444d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b444d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b444d-119">-Name</span></span>
<span data-ttu-id="b444d-120">등록 정의의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="b444d-121">-범위</span><span class="sxs-lookup"><span data-stu-id="b444d-121">-Scope</span></span>
<span data-ttu-id="b444d-122">등록 정의가 만들어진 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="b444d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b444d-123">CommonParameters</span></span>
<span data-ttu-id="b444d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b444d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b444d-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b444d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b444d-126">입력</span><span class="sxs-lookup"><span data-stu-id="b444d-126">INPUTS</span></span>

### <span data-ttu-id="b444d-127">않아야</span><span class="sxs-lookup"><span data-stu-id="b444d-127">None</span></span>
## <span data-ttu-id="b444d-128">출력</span><span class="sxs-lookup"><span data-stu-id="b444d-128">OUTPUTS</span></span>

### <span data-ttu-id="b444d-129">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="b444d-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="b444d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b444d-130">NOTES</span></span>

## <span data-ttu-id="b444d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b444d-131">RELATED LINKS</span></span>
