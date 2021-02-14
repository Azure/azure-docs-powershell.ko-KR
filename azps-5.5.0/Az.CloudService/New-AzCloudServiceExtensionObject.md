---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195137"
---
# <span data-ttu-id="5012c-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="5012c-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="5012c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5012c-102">SYNOPSIS</span></span>
<span data-ttu-id="5012c-103">확장에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="5012c-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="5012c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5012c-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="5012c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5012c-105">DESCRIPTION</span></span>
<span data-ttu-id="5012c-106">확장에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="5012c-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="5012c-107">예제</span><span class="sxs-lookup"><span data-stu-id="5012c-107">EXAMPLES</span></span>

### <span data-ttu-id="5012c-108">예제 1: Geneva 확장 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="5012c-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="5012c-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 Geneva 확장 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="5012c-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="5012c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5012c-111">PARAMETERS</span></span>

### <span data-ttu-id="5012c-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5012c-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5012c-113">CRP가 사용 가능해질 때 typeHandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5012c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5012c-114">-Name</span></span>
<span data-ttu-id="5012c-115">이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-115">Name.</span></span>

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

### <span data-ttu-id="5012c-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="5012c-116">-ProtectedSetting</span></span>
<span data-ttu-id="5012c-117">VM으로 보내기 전에 암호화되는 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="5012c-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5012c-118">-Publisher</span></span>
<span data-ttu-id="5012c-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="5012c-119">Publisher.</span></span>

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

### <span data-ttu-id="5012c-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="5012c-120">-RolesAppliedTo</span></span>
<span data-ttu-id="5012c-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="5012c-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5012c-122">-Setting</span><span class="sxs-lookup"><span data-stu-id="5012c-122">-Setting</span></span>
<span data-ttu-id="5012c-123">확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="5012c-124">-Type</span><span class="sxs-lookup"><span data-stu-id="5012c-124">-Type</span></span>
<span data-ttu-id="5012c-125">입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-125">Type.</span></span>

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

### <span data-ttu-id="5012c-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5012c-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="5012c-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="5012c-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="5012c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5012c-128">CommonParameters</span></span>
<span data-ttu-id="5012c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5012c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5012c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5012c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5012c-131">입력</span><span class="sxs-lookup"><span data-stu-id="5012c-131">INPUTS</span></span>

## <span data-ttu-id="5012c-132">출력</span><span class="sxs-lookup"><span data-stu-id="5012c-132">OUTPUTS</span></span>

### <span data-ttu-id="5012c-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="5012c-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="5012c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5012c-134">NOTES</span></span>

<span data-ttu-id="5012c-135">별칭</span><span class="sxs-lookup"><span data-stu-id="5012c-135">ALIASES</span></span>

## <span data-ttu-id="5012c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5012c-136">RELATED LINKS</span></span>

