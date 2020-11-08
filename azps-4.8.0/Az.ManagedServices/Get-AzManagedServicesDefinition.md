---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: a4a365cdaee79a39b87331c42c832e40f7cbd657
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213533"
---
# <span data-ttu-id="7c632-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c632-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="7c632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c632-102">SYNOPSIS</span></span>
<span data-ttu-id="7c632-103">등록 정의의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-103">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="7c632-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c632-104">SYNTAX</span></span>

### <span data-ttu-id="7c632-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c632-105">Default (Default)</span></span>
```
Get-AzManagedServicesDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c632-106">ById</span><span class="sxs-lookup"><span data-stu-id="7c632-106">ById</span></span>
```
Get-AzManagedServicesDefinition -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c632-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c632-107">ByResourceId</span></span>
```
Get-AzManagedServicesDefinition -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c632-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c632-108">DESCRIPTION</span></span>
<span data-ttu-id="7c632-109">등록 정의의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-109">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="7c632-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c632-110">EXAMPLES</span></span>

### <span data-ttu-id="7c632-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c632-111">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition

Name                                 ManagedByTenantId                    PrincipalId                                                                  RoleDefinitionId
----                                 -----------------                    -----------                                                                  ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
ee7e40e8-bc3f-4624-b0ca-d5364635b141 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
e2ddcd3c-d50f-4d51-afd9-f9132fcae4e7 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
d3301f65-7087-438c-a6bc-4b7ead094889 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
cae481c0-de7c-42a8-86c1-5b170861caf8 bab3375b-6197-4a15-a44b-16c41faa91d7 {d6f6c88a-5b7a-455e-ba40-ce146d4d3671, d6f6c88a-5b7a-455e-ba40-ce146d4d3671} {acdd72a7-3385-48ef-bd42-f606fba81ae7, b24988ac-6180-42a0-ab88-20f7382dd24c}
bb2626be-3e11-442f-b0f1-9209508d4f52 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="7c632-112">모든 등록 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-112">Gets all registration definitions.</span></span>

### <span data-ttu-id="7c632-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c632-113">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition -Id fff287a4-1714-4a17-bc40-a17ca8e69e3f

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="7c632-114">Id가 지정 된 등록 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-114">Gets the registration definition given its id.</span></span>

### <span data-ttu-id="7c632-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7c632-115">Example 3</span></span>
```powershell
PS C:\> $definitions = Get-AzManagedServicesDefinition
PS C:\> $definitions[0].Id
/subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/fff287a4-1714-4a17-bc40-a17ca8e69e3f
PS C:\> Get-AzManagedServicesDefinition -ResourceId $definitions[0].Id

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="7c632-116">정규화 된 리소스 id로 지정 된 등록 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-116">Gets the registration definition given the fully qualified resource id.</span></span>

## <span data-ttu-id="7c632-117">변수</span><span class="sxs-lookup"><span data-stu-id="7c632-117">PARAMETERS</span></span>

### <span data-ttu-id="7c632-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c632-118">-DefaultProfile</span></span>
<span data-ttu-id="7c632-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c632-120">-Id</span><span class="sxs-lookup"><span data-stu-id="7c632-120">-Id</span></span>
<span data-ttu-id="7c632-121">등록 정의 식별자 (예: b0c052e5-c437-4771-a476-8b1201158a57)입니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-121">The registration definition identifier (for example, b0c052e5-c437-4771-a476-8b1201158a57).</span></span>
```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c632-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c632-122">-ResourceId</span></span>
<span data-ttu-id="7c632-123">등록 정의의 정규화 된 리소스 id입니다 (예:/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="7c632-123">The fully qualified resource id of the registration definition (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="7c632-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c632-124">CommonParameters</span></span>
<span data-ttu-id="7c632-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c632-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c632-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c632-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c632-127">입력</span><span class="sxs-lookup"><span data-stu-id="7c632-127">INPUTS</span></span>

### <span data-ttu-id="7c632-128">않아야</span><span class="sxs-lookup"><span data-stu-id="7c632-128">None</span></span>

## <span data-ttu-id="7c632-129">출력</span><span class="sxs-lookup"><span data-stu-id="7c632-129">OUTPUTS</span></span>

### <span data-ttu-id="7c632-130">Microsoft. PowerShell. a m a.</span><span class="sxs-lookup"><span data-stu-id="7c632-130">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="7c632-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7c632-131">NOTES</span></span>

## <span data-ttu-id="7c632-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c632-132">RELATED LINKS</span></span>
