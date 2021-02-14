---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181788"
---
# <span data-ttu-id="9d813-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="9d813-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="9d813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d813-102">SYNOPSIS</span></span>
<span data-ttu-id="9d813-103">CloudServiceRoleProfileProperties에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9d813-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9d813-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d813-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d813-105">설명</span><span class="sxs-lookup"><span data-stu-id="9d813-105">DESCRIPTION</span></span>
<span data-ttu-id="9d813-106">CloudServiceRoleProfileProperties에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9d813-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9d813-107">예제</span><span class="sxs-lookup"><span data-stu-id="9d813-107">EXAMPLES</span></span>

### <span data-ttu-id="9d813-108">예제 1: 역할 프로필 속성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9d813-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="9d813-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 역할 프로필 속성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9d813-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="9d813-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="9d813-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="9d813-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d813-111">PARAMETERS</span></span>

### <span data-ttu-id="9d813-112">-Name</span><span class="sxs-lookup"><span data-stu-id="9d813-112">-Name</span></span>
<span data-ttu-id="9d813-113">역할 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d813-113">Name of role profile.</span></span>

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

### <span data-ttu-id="9d813-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9d813-114">-SkuCapacity</span></span>
<span data-ttu-id="9d813-115">클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d813-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d813-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9d813-116">-SkuName</span></span>
<span data-ttu-id="9d813-117">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d813-117">The sku name.</span></span>

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

### <span data-ttu-id="9d813-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9d813-118">-SkuTier</span></span>
<span data-ttu-id="9d813-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="9d813-119">SkuTier.</span></span>

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

### <span data-ttu-id="9d813-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d813-120">CommonParameters</span></span>
<span data-ttu-id="9d813-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d813-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d813-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d813-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d813-123">입력</span><span class="sxs-lookup"><span data-stu-id="9d813-123">INPUTS</span></span>

## <span data-ttu-id="9d813-124">출력</span><span class="sxs-lookup"><span data-stu-id="9d813-124">OUTPUTS</span></span>

### <span data-ttu-id="9d813-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9d813-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9d813-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d813-126">NOTES</span></span>

<span data-ttu-id="9d813-127">별칭</span><span class="sxs-lookup"><span data-stu-id="9d813-127">ALIASES</span></span>

## <span data-ttu-id="9d813-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d813-128">RELATED LINKS</span></span>

