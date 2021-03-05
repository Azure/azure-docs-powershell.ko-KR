---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: 6eec8f849d555fd2bf71f564c2e5c3ed9c699d80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978800"
---
# <span data-ttu-id="d34f4-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="d34f4-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="d34f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d34f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d34f4-103">CloudServiceRoleProfileProfileProperties에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d34f4-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="d34f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="d34f4-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="d34f4-105">설명</span><span class="sxs-lookup"><span data-stu-id="d34f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d34f4-106">CloudServiceRoleProfileProfileProperties에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d34f4-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="d34f4-107">예제</span><span class="sxs-lookup"><span data-stu-id="d34f4-107">EXAMPLES</span></span>

### <span data-ttu-id="d34f4-108">예제 1: 역할 프로필 속성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d34f4-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="d34f4-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 역할 프로필 속성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d34f4-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="d34f4-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="d34f4-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="d34f4-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d34f4-111">PARAMETERS</span></span>

### <span data-ttu-id="d34f4-112">-Name</span><span class="sxs-lookup"><span data-stu-id="d34f4-112">-Name</span></span>
<span data-ttu-id="d34f4-113">역할 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d34f4-113">Name of role profile.</span></span>

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

### <span data-ttu-id="d34f4-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d34f4-114">-SkuCapacity</span></span>
<span data-ttu-id="d34f4-115">클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d34f4-115">Specifies the number of role instances in the cloud service.</span></span>

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

### <span data-ttu-id="d34f4-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d34f4-116">-SkuName</span></span>
<span data-ttu-id="d34f4-117">sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d34f4-117">The sku name.</span></span>

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

### <span data-ttu-id="d34f4-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d34f4-118">-SkuTier</span></span>
<span data-ttu-id="d34f4-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="d34f4-119">SkuTier.</span></span>

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

### <span data-ttu-id="d34f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34f4-120">CommonParameters</span></span>
<span data-ttu-id="d34f4-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d34f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34f4-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d34f4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34f4-123">입력</span><span class="sxs-lookup"><span data-stu-id="d34f4-123">INPUTS</span></span>

## <span data-ttu-id="d34f4-124">출력</span><span class="sxs-lookup"><span data-stu-id="d34f4-124">OUTPUTS</span></span>

### <span data-ttu-id="d34f4-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProfileProperties</span><span class="sxs-lookup"><span data-stu-id="d34f4-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="d34f4-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d34f4-126">NOTES</span></span>

<span data-ttu-id="d34f4-127">별칭</span><span class="sxs-lookup"><span data-stu-id="d34f4-127">ALIASES</span></span>

## <span data-ttu-id="d34f4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d34f4-128">RELATED LINKS</span></span>

